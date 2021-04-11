---
title: Propiedad ConnectionOptions. Password (WSManDisp. h)
description: Establece la contraseña de una cuenta de dominio o local en el equipo remoto. Esta propiedad determina la contraseña para la autenticación.
ms.assetid: 61ba54b6-7da0-423e-b5b2-c4dd8aacd042
ms.tgt_platform: multiple
keywords:
- Propiedad password Administración remota de Windows
- Propiedad password Administración remota de Windows, objeto ConnectionOptions
- Administración remota de Windows de objeto ConnectionOptions, propiedad Password
topic_type:
- apiref
api_name:
- ConnectionOptions.Password
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4d553bf3f2a0a245e358e09a89eb1c00751e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150588"
---
# <a name="connectionoptionspassword-property"></a>ConnectionOptions. Password (propiedad)

Establece la contraseña de una cuenta de dominio o local en el equipo remoto. Esta propiedad determina la contraseña para la autenticación. Para obtener más información, consulte [autenticación para conexiones remotas](authentication-for-remote-connections.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
ConnectionOptions.Password As String
```



## <a name="property-value"></a>Valor de propiedad

Cadena que contiene la contraseña de una cuenta de dominio o local en el equipo remoto.

Si no se proporciona ningún valor y no se establece la marca **WSManFlagCredUsernamePassword** , se usa la contraseña de la cuenta que ejecuta el script.

Si no se proporciona ningún valor y se establece la marca **WSManFlagCredUsernamePassword** , el script le pedirá al usuario que escriba la contraseña (y el nombre de usuario, si no se proporciona). Si no se especifica un nombre de usuario y una contraseña válidos, se devuelve un error de acceso denegado.

## <a name="remarks"></a>Observaciones

Tenga en cuenta que no puede recuperar la contraseña. La contraseña solo se puede establecer con esta propiedad.

Si crea un objeto [**ConnectionOptions**](connectionoptions.md) y usa un nombre de usuario y una contraseña para conectarse a administración remota de Windows, se debe establecer la marca **WSManFlagCredUserNamePassword** en la llamada a [**WSMan. createSession**](wsman-createsession.md).

Para obtener más información sobre la configuración de contraseñas, vea la sección Comentarios en [**ConnectionOptions**](connectionoptions.md).

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se crea un objeto [**ConnectionOptions**](connectionoptions.md) y se establece la **contraseña**.


```VB
' Create a WSMan object. 
Set objWsman = CreateObject( "WSMAN.Automation" )
' Create a ConnectionOptions object
Set objOptions = objWSMan.CreateConnectionOptions
objOptions.Password = "<password>"
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





