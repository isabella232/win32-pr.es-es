---
title: Método External.download
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método de descarga inicia la descarga de un conjunto de elementos multimedia.
ms.assetid: 10bae41c-0658-4712-8a7e-375a1ec6dc25
keywords:
- descargar método Reproductor de Windows Media
- download method Reproductor de Windows Media , External (Clase)
- Clase externa Reproductor de Windows Media , método de descarga
topic_type:
- apiref
api_name:
- External.download
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35ef0c6e6c32e8959e402080796f29a3860fe728
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241959"
---
# <a name="externaldownload-method"></a>Método External.download

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **método** de descarga inicia la descarga de un conjunto de elementos multimedia.

## <a name="syntax"></a>Sintaxis


```JScript
External.download(
  Type,
  IDs
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tipo* \[ En\]
</dt> <dd>

Constante [de ubicación de biblioteca](library-location-constants.md) que especifica el tipo de elemento que se va a descargar. Por ejemplo, CPTrackID especifica que se van a descargar una o varias pistas.

</dd> <dt>

*IDs (IDs)* \[ En\]
</dt> <dd>

**Cadena** que contiene los identificadores, delimitados por punto y coma, de los elementos multimedia que se descargarán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Descargar contenido multimedia**](downloading-media-content.md)
</dt> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.buy**](external-buy.md)
</dt> <dt>

[**IWMPContentPartner::D ownload**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)
</dt> </dl>

 

 





