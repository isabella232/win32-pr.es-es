---
title: Win32_RDMSJoinedNode clase
description: Representa un nodo de servidor administrado por Escritorio remoto Management Services (RDMS).
ms.assetid: 8751f3f7-dfb5-45bd-a6b1-758aa22a3569
ms.tgt_platform: multiple
keywords:
- Win32_RDMSJoinedNode clase Servicios de Escritorio remoto
- Win32_RDMSJoinedNode clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode.FQDN
- Win32_RDMSJoinedNode.SID
- Win32_RDMSJoinedNode.OSVersion
- Win32_RDMSJoinedNode.IsRdcb
- Win32_RDMSJoinedNode.IsRdg
- Win32_RDMSJoinedNode.IsRdls
- Win32_RDMSJoinedNode.IsRdvh
- Win32_RDMSJoinedNode.IsRdwa
- Win32_RDMSJoinedNode.IsRdsh
- Win32_RDMSJoinedNode.IsWebAccessCertificateInstalled
- Win32_RDMSJoinedNode.IsGatewayCertificateInstalled
- Win32_RDMSJoinedNode.IsRedirectorCertificateInstalled
- Win32_RDMSJoinedNode.IsPublishingCertificateInstalled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e82a515f556c7193ef376972c5a8786dd0aaaafd7bcec3a56bf43244ea72a739
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868135"
---
# <a name="win32_rdmsjoinednode-class"></a>Clase \_ RDMSJoinedNode de Win32

Representa un nodo de servidor administrado por Escritorio remoto Management Services (RDMS).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSJoinedNode
{
  string  FQDN;
  string  SID;
  String  OSVersion;
  boolean IsRdcb;
  boolean IsRdg;
  boolean IsRdls;
  boolean IsRdvh;
  boolean IsRdwa;
  boolean IsRdsh;
  boolean IsWebAccessCertificateInstalled;
  boolean IsGatewayCertificateInstalled;
  boolean IsRedirectorCertificateInstalled;
  boolean IsPublishingCertificateInstalled;
};
```

## <a name="members"></a>Miembros

La **clase \_ RDMSJoinedNode de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ RDMSJoinedNode de Win32** tiene estos métodos.



| Método                                                                | Descripción                                                                                                                                                                                           |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetJoinedNodeCount**](win32-rdmsjoinednode-getjoinednodecount.md) | **Windows Server 2012 R2 y Windows Server 2012:** Este método no está disponible antes de Windows Server 2016.<br/> Obtiene el número de servidores que tienen instalado el rol especificado.<br/> |
| [**Combinar**](join-win32-rdmsjoinednode.md)                             | Agrega un nodo a RDMS.<br/>                                                                                                                                                                       |
| [**Unjoin (Unjoin)**](unjoin-win32-rdmsjoinednode.md)                         | Quita un nodo de RDMS.<br/>                                                                                                                                                                  |



 

### <a name="properties"></a>Propiedades

La **clase \_ RDMSJoinedNode de Win32** tiene estas propiedades.

<dl> <dt>

**FQDN**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Obtiene el nombre de dominio completo del nodo.

</dd> <dt>

**IsGatewayCertificateInstalled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor tiene un certificado para realizar la autenticación para las conexiones de Escritorio remoto puerta de enlace. **TRUE** si el certificado está instalado; de lo contrario, **FALSE**.

</dd> <dt>

**IsPublishingCertificateInstalled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor tiene un certificado para firmar Protocolo de escritorio remoto archivos de publicación. **TRUE** si el certificado está instalado; de lo contrario, **FALSE**.

</dd> <dt>

**IsRdcb**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor está Conexión a Escritorio remoto Broker. **TRUE** si el servidor es un Conexión a Escritorio remoto Broker; de lo contrario, **FALSE**.

</dd> <dt>

**IsRdg**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor está Escritorio remoto de puerta de enlace. **TRUE** si el servidor es un servidor Escritorio remoto puerta de enlace; de lo contrario, **FALSE**.

</dd> <dt>

**IsRdls**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor está Escritorio remoto servidor de licencias. **TRUE** si el servidor es un Escritorio remoto de licencias; de lo contrario, **FALSE**.

</dd> <dt>

**IsRdsh**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor está Escritorio remoto servidor host de sesión. **TRUE** si el servidor es un servidor Escritorio remoto host de sesión; de lo contrario, **FALSE**.

</dd> <dt>

**IsRdvh**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor está Escritorio remoto host de virtualización. **TRUE** si el servidor es un host de Escritorio remoto virtualización; de lo contrario, **FALSE**.

</dd> <dt>

**IsRdwa**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor está Escritorio remoto servidor de acceso web. **TRUE** si el servidor es un servidor Escritorio remoto Web Access; de lo contrario, **FALSE**.

</dd> <dt>

**IsRedirectorCertificateInstalled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor tiene un certificado para realizar la autenticación Servicios de Escritorio remoto implementación. **TRUE** si el certificado está instalado; de lo contrario, **FALSE**.

</dd> <dt>

**IsWebAccessCertificateInstalled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor tiene un certificado para realizar la autenticación Escritorio remoto Web Access. **TRUE** si el certificado está instalado; de lo contrario, **FALSE**.

</dd> <dt>

**OSVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **String**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Obtiene y establece la versión de los sistemas operativos del nodo.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Obtiene el identificador de seguridad (SID) del nodo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | Rdms \\ cimv2 \\ raíz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Escritorio remoto Management Services Provider](rdms-api-reference.md)
</dt> </dl>

 

