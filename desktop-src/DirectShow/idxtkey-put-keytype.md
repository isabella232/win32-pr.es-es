---
description: El método put \_ KeyType especifica el tipo de clave.
ms.assetid: 4a6201e6-1939-4da6-8c9f-1c34b9713ecb
title: Método IDxtKey::p ut_KeyType (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8e5e501c1f678adb857e39d579fbd958127652a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361331"
---
# <a name="idxtkeyput_keytype-method"></a>Método IDxtKey::p ut \_ KeyType

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `put_KeyType` método especifica el tipo de clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_KeyType(
  [in] int newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* \[ En\]
</dt> <dd>

Especifica el tipo de clave. Este parámetro debe ser uno de los siguientes valores de enumeración.



| Value             | Descripción                                           |
|-------------------|-------------------------------------------------------|
| DXTKEY \_ RGB       | Clave de exclusión. (Clave en el valor RGB).                       |
| DXTKEY \_ NONRED    | Clave nored. (Hace que las áreas azul y verde sea transparente). |
| DXTKEY \_ LUMINANCE | Tecla de luminosidad.                                        |
| DXTKEY \_ ALPHA     | Clave por valor alfa.                                   |
| DXTKEY \_ HUE       | Clave por matiz.                                           |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDxtKey (interfaz)**](idxtkey.md)
</dt> </dl>

 

 




