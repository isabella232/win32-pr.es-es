---
title: Método Media.getAttributeCountByType
description: El método getAttributeCountByType recupera el número de atributos asociados con el nombre de atributo y el idioma especificados.
ms.assetid: 5644e823-a9b1-4b02-9dd6-015e524fde64
keywords:
- Método getAttributeCountByType Reproductor de Windows Media
- Método getAttributeCountByType Reproductor de Windows Media , clase Media
- Clase media Reproductor de Windows Media método , getAttributeCountByType
topic_type:
- apiref
api_name:
- Media.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613dca43c32322cd5e7de2b2b04605789009cbf6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068424"
---
# <a name="mediagetattributecountbytype-method"></a>Método Media.getAttributeCountByType

El **método getAttributeCountByType** recupera el número de atributos asociados con el nombre de atributo y el idioma especificados.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Media.getAttributeCountByType(
  name,
  language
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*name* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo. Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la referencia Reproductor de Windows Media [atributo](attribute-reference.md).

</dd> <dt>

*idioma* \[ En\]
</dt> <dd>

**Cadena** que representa el idioma. Si el valor se establece en null o "" (cadena vacía), se usa la cadena de configuración regional actual. De lo contrario, el valor debe ser una cadena de idioma RFC 1766 válida, como "en-us".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor Number** (**long**) que contiene el recuento de atributos.

## <a name="remarks"></a>Observaciones

Este método se usa para determinar el número de atributos correspondientes a un nombre de atributo determinado para un objeto **Media** determinado. Los números de índice se pueden pasar al **método getItemInfoByType.** Esto resulta útil, por ejemplo, cuando un elemento multimedia se ha clasificado en varios géneros.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

**Reproductor de Windows Media 10 Mobile:** Esta propiedad siempre devuelve 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MediaObject**](media-object.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





