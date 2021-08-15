---
title: IWMPStringCollection2 getAttributeCountByType (método)
description: El método getAttributeCountByType devuelve el número de atributos asociados al índice de la colección de cadenas, el nombre de atributo y el idioma especificados.
ms.assetid: 30312039-3676-4322-b6f6-fb86098bf578
keywords:
- Método getAttributeCountByType Reproductor de Windows Media
- Método getAttributeCountByType Reproductor de Windows Media , interfaz IWMPStringCollection2
- Interfaz IWMPStringCollection2 Reproductor de Windows Media método , getAttributeCountByType
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c236d03cad0612d8306b8ccde370136cb9b31acca82e0aa52761ed56fb4b9bb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330919"
---
# <a name="iwmpstringcollection2getattributecountbytype-method"></a>IWMPStringCollection2::getAttributeCountByType (método)

El **método getAttributeCountByType** devuelve el número de atributos asociados al índice de la colección de cadenas, el nombre de atributo y el idioma especificados.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 getAttributeCountByType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPStringCollection2.getAttributeCountByType
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*lCollectionIndex* \[ En\]
</dt> <dd>

**System.Int32 que especifica** el índice de base cero del elemento de colección de cadenas del que se va a obtener el atributo.

</dd> <dt>

*bstrType* \[ En\]
</dt> <dd>

**System.String que** es el nombre del atributo.

</dd> <dt>

*bstrLanguage* \[ En\]
</dt> <dd>

**System.String que** es el nombre del idioma. Si el valor se establece en null o en una cadena de longitud cero (""), se usa la cadena de configuración regional actual. De lo contrario, el valor debe ser una cadena de lenguaje RFC 1766 válida, como "en-us".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.Int32** que es el recuento.

## <a name="remarks"></a>Comentarios

Este método se usa para detectar el número de atributos correspondientes a un nombre de atributo determinado para un elemento **StringCollection** determinado. A continuación, los números de índice se pueden pasar al cuarto parámetro del **método getItemInfoByType.**

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMPStringCollection2 (VB y C#)**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2.getItemInfoByType (VB y C#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





