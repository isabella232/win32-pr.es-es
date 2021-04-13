---
title: Win32_RDMSJoinedNode (clase)
description: Representa un nodo de servidor administrado por Escritorio remoto Management Services (RDMS).
ms.assetid: 8751f3f7-dfb5-45bd-a6b1-758aa22a3569
ms.tgt_platform: multiple
keywords:
- Win32_RDMSJoinedNode clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDMSJoinedNode de clase, se describe
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
ms.openlocfilehash: cabf1cf7ff98b698624285b2877412c4323259b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421965"
---
# <a name="win32_rdmsjoinednode-class"></a>\_Clase Win32 RDMSJoinedNode

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

La clase **Win32 \_ RDMSJoinedNode** tiene estos métodos.



| Método                                                                | Descripción                                                                                                                                                                                           |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetJoinedNodeCount**](win32-rdmsjoinednode-getjoinednodecount.md) | **Windows server 2012 R2 y Windows server 2012:** Este método no está disponible antes de Windows Server 2016.<br/> Obtiene el número de servidores que tienen el rol especificado instalado.<br/> |
| [**Combinar**](join-win32-rdmsjoinednode.md)                             | Agrega un nodo a RDMS.<br/>                                                                                                                                                                       |
| [**Separarse**](unjoin-win32-rdmsjoinednode.md)                         | Quita un nodo de RDMS.<br/>                                                                                                                                                                  |



 

### <a name="properties"></a>Propiedades

La **clase \_ RDMSJoinedNode de Win32** tiene estas propiedades.

<dl> <dt>

**FQDN**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Obtiene el nombre de dominio completo del nodo.

</dd> <dt>

**IsGatewayCertificateInstalled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor tiene un certificado para realizar la autenticación para Escritorio remoto conexiones de puerta de enlace. **True** si el certificado está instalado; en caso contrario, **false**.

</dd> <dt>

**IsPublishingCertificateInstalled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor tiene un certificado para firmar Protocolo de escritorio remoto archivos de publicación. **True** si el certificado está instalado; en caso contrario, **false**.

</dd> <dt>

**IsRdcb**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor está Conexión a Escritorio remoto Broker. **True** si el servidor es un agente de conexión a escritorio remoto; en caso contrario, **false**.

</dd> <dt>

**IsRdg**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor está Escritorio remoto servidor de puerta de enlace. **True** si el servidor es un servidor de puerta de enlace de escritorio remoto; en caso contrario, **false**.

</dd> <dt>

**IsRdls**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor está Escritorio remoto servidor de licencias. **True** si el servidor es un servidor de licencias de escritorio remoto; en caso contrario, **false**.

</dd> <dt>

**IsRdsh**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor es Escritorio remoto servidor host de sesión. **True** si el servidor es un servidor host de sesión escritorio remoto; en caso contrario, **false**.

</dd> <dt>

**IsRdvh**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor está Escritorio remoto host de virtualización. **True** si el servidor es un host de virtualización de escritorio remoto; en caso contrario, **false**.

</dd> <dt>

**IsRdwa**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor está Escritorio remoto servidor de acceso web. **True** si el servidor es un servidor de escritorio remoto Web Access; en caso contrario, **false**.

</dd> <dt>

**IsRedirectorCertificateInstalled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor tiene un certificado para realizar la autenticación para Servicios de Escritorio remoto implementación. **True** si el certificado está instalado; en caso contrario, **false**.

</dd> <dt>

**IsWebAccessCertificateInstalled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Obtiene y establece un valor que indica si el servidor tiene un certificado para realizar la autenticación para Escritorio remoto acceso web. **True** si el certificado está instalado; en caso contrario, **false**.

</dd> <dt>

**OSVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Obtiene y establece la versión de los sistemas operativos en el nodo.

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
| Espacio de nombres<br/>                | RDMs raíz de \\ cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Proveedor de servicios de administración de Escritorio remoto](rdms-api-reference.md)
</dt> </dl>

 

