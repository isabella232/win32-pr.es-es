---
title: Método CreateSelfSignedCertificate de la clase Win32_TSGatewayServer
description: Crea un certificado autofirmado y devuelve el hash del certificado como \ 0034; out \ 0034; parámetro.
ms.assetid: 2a5b8dee-50b8-44b7-9e29-25aff1c40f5d
ms.tgt_platform: multiple
keywords:
- Método CreateSelfSignedCertificate Servicios de Escritorio remoto
- Método CreateSelfSignedCertificate Servicios de Escritorio remoto, clase Win32_TSGatewayServer
- Win32_TSGatewayServer de clase Servicios de Escritorio remoto, método CreateSelfSignedCertificate
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
ms.openlocfilehash: 4258566856a5fbc277053b65afe972751855d831
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489532"
---
# <a name="createselfsignedcertificate-method-of-the-win32_tsgatewayserver-class"></a>Método CreateSelfSignedCertificate de la \_ clase TSGatewayServer de Win32

Crea un certificado autofirmado y devuelve el hash del certificado como un parámetro "out". Además, agrega el texto " \_ \_ certificado autofirmado de puerta de enlace de TS \_ \_ " a la propiedad de contexto de certificado para que el certificado se reconozca como un certificado de puerta de enlace de escritorio remoto (puerta de enlace de escritorio remoto). Este método usa un contenedor de claves específico de puerta de enlace de escritorio remoto para crear el certificado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CreateSelfSignedCertificate(
  [in]  string SubjectName,
  [out] uint8  CertHash[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SubjectName* \[ de\]
</dt> <dd>

Nombre del firmante del certificado autofirmado.

</dd> <dt>

*CertHash* \[ enuncia\]
</dt> <dd>

El hash del certificado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para llamar a este método, debe ser miembro del grupo administradores.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayServer**](win32-tsgatewayserver.md)
</dt> </dl>

 

