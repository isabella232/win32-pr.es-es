---
title: External. download (método)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método download inicia la descarga de un conjunto de elementos multimedia.
ms.assetid: 10bae41c-0658-4712-8a7e-375a1ec6dc25
keywords:
- método de descarga de Windows Media Player
- método de descarga de Windows Media Player, clase externa
- Clase externa Windows Media Player, método download
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698597"
---
# <a name="externaldownload-method"></a>External. download (método)

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El método **download** inicia la descarga de un conjunto de elementos multimedia.

## <a name="syntax"></a>Sintaxis


```JScript
External.download(
  Type,
  IDs
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tipo* \[ de de\]
</dt> <dd>

Una [constante de ubicación de biblioteca](library-location-constants.md) que especifica el tipo de elemento que se va a descargar. Por ejemplo, CPTrackID especifica que se van a descargar una o más pistas.

</dd> <dt>

*Identificadores* \[ de\]
</dt> <dd>

**Cadena** que contiene los identificadores, delimitados por punto y coma, de los elementos multimedia que se van a descargar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Descargar contenido multimedia**](downloading-media-content.md)
</dt> <dt>

[**Objeto externo para las tiendas en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. Buy**](external-buy.md)
</dt> <dt>

[**IWMPContentPartner::D scargar**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)
</dt> </dl>

 

 





