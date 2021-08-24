---
title: Método CreateSelfSignedCertificate de la Win32_TSGatewayServer clase
description: Crea un certificado autofirmado y devuelve el hash del certificado como \ 0034;out \ 0034; Parámetro.
ms.assetid: 2a5b8dee-50b8-44b7-9e29-25aff1c40f5d
ms.tgt_platform: multiple
keywords:
- Método CreateSelfSignedCertificate Servicios de Escritorio remoto
- Método CreateSelfSignedCertificate Servicios de Escritorio remoto , Win32_TSGatewayServer clase
- Win32_TSGatewayServer clase Servicios de Escritorio remoto , método CreateSelfSignedCertificate
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.CreateSelfSignedCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 200b08da8d5eea9f31405a357650384081c407df4eb76820cd47a111e6b66aab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139058"
---
# <a name="createselfsignedcertificate-method-of-the-win32_tsgatewayserver-class"></a>Método CreateSelfSignedCertificate de la clase \_ TSGatewayServer de Win32

Crea un certificado autofirmado y devuelve el hash del certificado como un parámetro "out". Además, agrega el texto "TS GATEWAY SELF SIGNED CERTIFICATE" a la propiedad de contexto del certificado para que el certificado se reconozca como un certificado de puerta de enlace de Escritorio remoto (puerta de \_ \_ enlace de Escritorio \_ \_ remoto). Este método usa un contenedor de claves específico de puerta de enlace de Escritorio remoto para crear el certificado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CreateSelfSignedCertificate(
  [in]  string SubjectName,
  [out] uint8  CertHash[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SubjectName* \[ En\]
</dt> <dd>

Nombre de sujeto del certificado autofirmado.

</dd> <dt>

*CertHash* \[ out\]
</dt> <dd>

Hash del certificado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSGatewayServer de Win32 \_**](win32-tsgatewayserver.md)
</dt> </dl>

 

