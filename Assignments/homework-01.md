

## Name:
Sapna Patil

## Ip Address
http://67.205.143.154/

## Phpmyadmin Link
http://205.143.154/phpmyadmin

## Table Create statements

## gift_options.sql

``` 
CREATE TABLE IF NOT EXISTS `gift_options` (
       	`allowGiftWrap` Boolean  NOT NULL,
       	`allowGiftMessage` Boolean NOT NULL,
       	`allowGiftReceipt` Boolean NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
```

## image_entities.sql
```
CREATE TABLE IF NOT EXISTS `image_entities` (
        `thumbnailImage` varchar(149) NOT NULL,
        `mediumImage` varchar(149) NOT NULL,
        `largeImage` varchar(149) NOT NULL,
        `entityType` varchar(9) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
```



## To add Primary key
```
ALTER TABLE `image_entities` ADD PRIMARY KEY ( `entityType` ) ;
```

## market_place_price.sql
```
CREATE TABLE IF NOT EXISTS `market_place_price` (
        `price` double NOT NULL,
        `sellerInfo` varchar(44) NOT NULL,
        `standardShipRate`double NOT NULL,
        `twoThreeDayShippingRate`double NOT NULL,
        `availableOnline` boolean NOT NULL,
        `clearance`boolean NOT NULL,
        `offerType`varchar(16) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
```

## To add Primary key
``` ALTER TABLE `market_place_price` ADD PRIMARY KEY ( `price` ) ; ```

## products.sql
```
CREATE TABLE IF NOT EXISTS `products` (
        `itemId`int(9) NOT NULL,
        `parentItemId` int(9) NOT NULL,
        `name`varchar(200) NOT NULL,
        `salePrice`double NOT NULL,
        `upc`varchar(200) NOT NULL,
        `categoryPath` varchar(123) NOT NULL,
        `shortDescription` varchar(112) NOT NULL,
        `longDescription` varchar(5540) NOT NULL,
        `brandName` varchar(36) NOT NULL,
        `thumbnailImage` varchar(149) NOT NULL,
        `mediumImage`varchar(149) NOT NULL,
        `largeImage` varchar(149) NOT NULL,
        `productTrackingUrl`varchar(416) NOT NULL,
        `modelNumber`varchar(53) NOT NULL,
        `productUrl`varchar(345) NOT NULL,
        `categoryNode` varchar(23) NOT NULL,
        `stock` varchar(13) NOT NULL,
        `addToCartUrl`varchar(221) NOT NULL,
        `affiliateAddToCartUrl` varchar(296) NOT NULL,
        `offerType`varchar(16) NOT NULL,
        `msrp` double NOT NULL,
        `standardShipRate` double NOT NULL,
        `color` varchar(10) NOT NULL,
        `customerRating`varchar(5) NOT NULL,
        `numReviews` int(5) NOT NULL,
        `customerRatingImage`varchar(48) NOT NULL,
        `maxItemsInOrder` int(6) NOT NULL,
        `size`varchar(49) NOT NULL,
        `sellerInfo`varchar(44) NOT NULL,
        `age`varchar(14) NOT NULL,
        `gender`varchar(6) NOT NULL,
        `isbn` varchar(13) NOT NULL,
        `preOrderShipsOn`varchar(19) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
```

## To add Primary key
```
ALTER TABLE `products` 
ADD PRIMARY KEY ( `itemId` , `parentItemId` ) ;
```
