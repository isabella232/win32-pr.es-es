---
title: DownloadCollection.id
description: Nota En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad id recupera el identificador de la colección de descarga.
ms.assetid: b5b17f22-913c-4055-8958-e3efac819b2b
keywords:
- DownloadCollection.id Reproductor de Windows Media
topic_type:
- apiref
api_name:
- DownloadCollection.id
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e505db2e643286f84b61bfa8604b9edc8ef36fa39cdd040bd9cc49bb98f82d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651275"
---
# <a name="downloadcollectionid"></a>DownloadCollection.id

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La **propiedad id** recupera el identificador de la colección de descarga.

## <a name="syntax"></a>Syntax

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).id
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Comentarios

Cuando el Administrador de descarga crea una nueva recopilación de descarga, asigna a la colección un número de identificador. Los números de identificador persisten entre Reproductor de Windows Media y las sesiones del sistema operativo.

Los números de identificador no son únicos. Sin embargo, hay suficientes números de identificador disponibles en el valor de 32 bits que es muy poco probable que uno nuevo sobrescriba un número de identificador existente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/>                                  |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DownloadCollection (objeto)**](downloadcollection-object.md)
</dt> </dl>

 

 





