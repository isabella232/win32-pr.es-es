---
title: Propiedad ConnectionOptions.Password (WSManDisp.h)
description: Establece la contraseña de una cuenta local o de dominio en el equipo remoto. Esta propiedad determina la contraseña para la autenticación.
ms.assetid: 61ba54b6-7da0-423e-b5b2-c4dd8aacd042
ms.tgt_platform: multiple
keywords:
- Propiedad Password Windows Remote Management
- Propiedad Password Windows administración remota, objeto ConnectionOptions
- Objeto ConnectionOptions Windows administración remota, propiedad Password
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
ms.openlocfilehash: 8ffc992b5a0560175d6562a16cf4cb3fd6bc4259eb3b712e26708dc713baba14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898995"
---
# <a name="connectionoptionspassword-property"></a>Propiedad ConnectionOptions.Password

Establece la contraseña de una cuenta local o de dominio en el equipo remoto. Esta propiedad determina la contraseña para la autenticación. Para obtener más información, vea [Autenticación para conexiones remotas.](authentication-for-remote-connections.md)

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
ConnectionOptions.Password As String
```



## <a name="property-value"></a>Valor de propiedad

Cadena que contiene la contraseña de una cuenta local o de dominio en el equipo remoto.

Si no se proporciona ningún valor y no se establece la marca **WSManFlagCredUsernamePassword,** se usa la contraseña de la cuenta que ejecuta el script.

Si no se proporciona ningún valor y se establece la marca **WSManFlagCredUsernamePassword,** el script solicita al usuario que escriba la contraseña (y el nombre de usuario, si no se proporciona). Si no se han especificado un nombre de usuario y una contraseña válidos, se devuelve un error de acceso denegado.

## <a name="remarks"></a>Comentarios

Tenga en cuenta que no puede recuperar la contraseña. La contraseña solo se puede establecer con esta propiedad.

Si crea un objeto [**ConnectionOptions**](connectionoptions.md) y usa un nombre de usuario y una contraseña para conectarse a la administración remota de Windows, la marca **WSManFlagCredUserNamePassword** debe establecerse en la llamada a [**WSMan.CreateSession**](wsman-createsession.md).

Para obtener más información sobre cómo establecer contraseñas, vea la sección Comentarios de [**ConnectionOptions.**](connectionoptions.md)

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se [**crea un objeto ConnectionOptions**](connectionoptions.md) y se establece **la contraseña**.


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
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





