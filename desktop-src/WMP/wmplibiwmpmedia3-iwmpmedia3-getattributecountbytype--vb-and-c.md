---
title: Método IWMPMedia3 getAttributeCountByType
description: El método getAttributeCountByType devuelve el número de atributos asociados al tipo de atributo especificado.
ms.assetid: d692635f-f9f1-4d8e-a9c5-9d7fa84f41bd
keywords:
- Método getAttributeCountByType Reproductor de Windows Media
- Método getAttributeCountByType Reproductor de Windows Media , interfaz IWMPMedia3
- Interfaz IWMPMedia3 Reproductor de Windows Media , método getAttributeCountByType
topic_type:
- apiref
api_name:
- IWMPMedia3.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c8e3fc681ea5471457bd9a80ac3e26dabc08b2112387dd8c5f785bf5f055dfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000115"
---
# <a name="iwmpmedia3getattributecountbytype-method"></a>IWMPMedia3::getAttributeCountByType (método)

El **método getAttributeCountByType** devuelve el número de atributos asociados al tipo de atributo especificado.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 getAttributeCountByType(
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPMedia3.getAttributeCountByType
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrType* \[ En\]
</dt> <dd>

**System.String que** es el tipo de atributo.

</dd> <dt>

*bstrLanguage* \[ En\]
</dt> <dd>

**System.String que** es el idioma. Si el valor se establece en null o en una cadena de longitud cero (""), se usa la cadena de configuración regional actual. De lo contrario, el valor debe ser una cadena de idioma RFC 1766 válida, como "en-us".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.Int32 que** es el recuento de atributos asociados al tipo.

## <a name="remarks"></a>Comentarios

Este método se usa para detectar el número de atributos correspondientes a un nombre de atributo determinado para un elemento multimedia determinado. Los números de índice se pueden pasar al **método getItemInfoByType.** Esto resulta útil, por ejemplo, cuando un elemento multimedia se ha clasificado en varios géneros.

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPMedia3 (VB y C#)**](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3.getItemInfoByType (VB y C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





