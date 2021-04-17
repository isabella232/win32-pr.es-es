---
title: IWMPMedia3 getAttributeCountByType, método
description: El método getAttributeCountByType devuelve el número de atributos asociados al tipo de atributo especificado.
ms.assetid: d692635f-f9f1-4d8e-a9c5-9d7fa84f41bd
keywords:
- método getAttributeCountByType de Windows Media Player
- método getAttributeCountByType Windows Media Player, interfaz IWMPMedia3
- Interfaz IWMPMedia3 Windows Media Player, método getAttributeCountByType
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
ms.openlocfilehash: 49505f9e9df8778cc2c17ba062da6700b9b8aec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670364"
---
# <a name="iwmpmedia3getattributecountbytype-method"></a>IWMPMedia3:: getAttributeCountByType (método)

El método **getAttributeCountByType** devuelve el número de atributos asociados al tipo de atributo especificado.

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

*bstrType* \[ de\]
</dt> <dd>

**System. String** que es el tipo de atributo.

</dd> <dt>

*bstrLanguage* \[ de\]
</dt> <dd>

**System. String** que es el idioma. Si el valor se establece en null o en una cadena de longitud cero (""), se usa la cadena de configuración regional actual. De lo contrario, el valor debe ser una cadena de idioma RFC 1766 válida, como "en-US".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System. Int32** que es el recuento de atributos asociados al tipo.

## <a name="remarks"></a>Observaciones

Este método se utiliza para detectar el número de atributos correspondientes a un nombre de atributo determinado para un elemento multimedia determinado. Después, los números de índice se pueden pasar al método **getItemInfoByType** . Esto resulta útil, por ejemplo, cuando un elemento multimedia se ha clasificado en varios géneros.

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPMedia3 (VB y C#)**](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB y C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





