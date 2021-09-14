---
description: El método get \_ Invert recupera un valor booleano que indica si se invierte la operación de clave. Esta propiedad se aplica a todos los tipos de clave excepto DXTKEY \_ ALPHA.
ms.assetid: 2ccf2066-3d9c-493b-bc54-a03e7d075531
title: Método IDxtKey::get_Invert (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 51b95758adf6690f6d4fa479ac1cc2c585fa9352
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361346"
---
# <a name="idxtkeyget_invert-method"></a>IDxtKey::get \_ Invert (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método recupera un valor booleano que indica si se invierte la operación `get_Invert` de clave. Esta propiedad se aplica a todos los tipos de clave excepto DXTKEY \_ ALPHA.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Invert(
  [out, retval] BOOL *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Recibe uno de los siguientes valores.



| Value     | Descripción                                                                       |
|-----------|-----------------------------------------------------------------------------------|
| **TRUE**  | Los píxeles de la imagen de sobrelying se invierten con respecto a la operación predeterminada. |
| **FALSE** | Los píxeles de la imagen de exceso se hacen transparentes de la manera predeterminada.         |



 

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

[**IDxtKey::get \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




