---
title: Win32_RDMSEnvironment (clase)
description: Administra un entorno de Escritorio remoto Management Services (RDMS).
ms.assetid: 8a3b10c1-d01d-4e52-8915-29159cc406cc
ms.tgt_platform: multiple
keywords:
- Win32_RDMSEnvironment clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDMSEnvironment de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a78acb964471844be74481d1ddfa2d4cf56a173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676710"
---
# <a name="win32_rdmsenvironment-class"></a>\_Clase Win32 RDMSEnvironment

Administra un entorno de Escritorio remoto Management Services (RDMS).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSEnvironment
{
};
```

## <a name="members"></a>Miembros

La **clase \_ RDMSEnvironment de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La clase **Win32 \_ RDMSEnvironment** tiene estos métodos.



| Método                                                                   | Descripción                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**GetActiveServer**](getactiveserver-win32-rdmsenvironment.md)         | Recupera el nombre de dominio completo (FQDN) del entorno de RDMS.<br/>                 |
| [**GetClientAccessName**](getclientaccessname-win32-rdmsenvironment.md) | Recupera el nombre del registro de recursos (RR) del sistema de nombres de dominio (DNS) del entorno de RDMS.<br/> |
| [**SetActiveServer**](setactiveserver-win32-rdmsenvironment.md)         | Establece el FQDN del entorno de RDMS en el nodo actual.<br/>                                |
| [**SetClientAccessName**](setclientaccessname-win32-rdmsenvironment.md) | Actualiza el nombre de DNS RR del entorno de RDMS.<br/>                                          |



 

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

 

 





