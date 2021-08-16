---
description: El método get \_ KeyType recupera el tipo de clave.
ms.assetid: 902cbd46-529a-45d8-afa2-a8dd9439769a
title: Método IDxtKey::get_KeyType (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cfb8930df859771f61406ebab9a1e7f60cfdf149eaf66eae23120bb7292ebf74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819479"
---
# <a name="idxtkeyget_keytype-method"></a>Método IDxtKey::get \_ KeyType

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `get_KeyType` método recupera el tipo de clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_KeyType(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Recibe uno de los siguientes valores de enumeración.



| Valor             | Descripción                                           |
|-------------------|-------------------------------------------------------|
| DXTKEY \_ RGB       | Clave de exclusión. (Clave en el valor RGB).                       |
| DXTKEY \_ NONRED    | Clave nored. (Hace que las áreas azul y verde sea transparente). |
| DXTKEY \_ LUMINANCE | Tecla de luminosidad.                                        |
| DXTKEY \_ ALPHA     | Clave por valor alfa.                                   |
| DXTKEY \_ HUE       | Clave por matiz.                                           |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDxtKey (interfaz)**](idxtkey.md)
</dt> </dl>

 

 




