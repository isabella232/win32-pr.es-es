---
description: El método put \_ Invert especifica si se invierte la operación de clave. Esta propiedad se aplica a todos los tipos de clave excepto DXTKEY \_ ALPHA.
ms.assetid: 06acdd9f-eb3a-49bd-961d-00966df2ccb4
title: Método IDxtKey::p ut_Invert (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3e4b807770d0eeb985c982b61b8390695cc42327
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361332"
---
# <a name="idxtkeyput_invert-method"></a>IDxtKey::p ut \_ Invert (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `put_Invert` método especifica si se invierte la operación de clave. Esta propiedad se aplica a todos los tipos de clave excepto DXTKEY \_ ALPHA.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Invert(
  [in] BOOL newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* \[ En\]
</dt> <dd>

Especifica un valor booleano. Si **es TRUE,** los píxeles de la imagen de sobrease se invierten con respecto a la operación predeterminada. Si **es FALSE,** los píxeles de la imagen de sobresaliendo se hacen transparentes de la manera predeterminada.

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
</dt> <dt>

[**IDxtKey::put \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




