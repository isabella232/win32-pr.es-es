---
description: El método \_ get Luminance recupera el valor de luminosidad en el que se va a claver. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ LUMINANCE.
ms.assetid: 92113331-a7b7-4618-81b2-ea02e7bcc923
title: Método IDxtKey::get_Luminance (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Luminance
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4035662f8510fd7caab6b2c540bb3194c218c83fde7ce5505c3f6c974394d2e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792375"
---
# <a name="idxtkeyget_luminance-method"></a>Método IDxtKey::get \_ Luminance

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `get_Luminance` método recupera el valor de luminosidad en el que se va a claver. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ LUMINANCE.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Luminance(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Recibe el valor de luminosidad en el que se va a claver.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDxtKey (interfaz)**](idxtkey.md)
</dt> <dt>

[**IDxtKey::get \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




