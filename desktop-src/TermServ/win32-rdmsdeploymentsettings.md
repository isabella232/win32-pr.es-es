---
title: Win32_RDMSDeploymentSettings (clase)
description: Administra la configuración de implementación de una colección de escritorios virtuales.
ms.assetid: c33563d5-a388-46d3-b23a-797aab9d472a
ms.tgt_platform: multiple
keywords:
- Win32_RDMSDeploymentSettings clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDMSDeploymentSettings de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6be75f74a71a82800bc6fdd7ba0c4bae5a85021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534011"
---
# <a name="win32_rdmsdeploymentsettings-class"></a>\_Clase Win32 RDMSDeploymentSettings

Administra la configuración de implementación de una colección de escritorios virtuales.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDeploymentSettings
{
};
```

## <a name="members"></a>Miembros

La **clase \_ RDMSDeploymentSettings de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La clase **Win32 \_ RDMSDeploymentSettings** tiene estos métodos.



| Método                                                                                                  | Descripción                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**GetBaseVHDPath**](getbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | Recupera la ruta de acceso base al directorio en el que se implementan los VHD de la colección de escritorios virtuales.<br/>                 |
| [**GetConnectionString**](win32-rdmsdeploymentsettings-getconnectionstring.md)                         | Recupera la cadena de conexión de base de datos de nivel de implementación.<br/>                                                             |
| [**GetDiffVHDPath**](getdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | Recupera la ruta de acceso al directorio en la que se implementan los discos de diferenciación para una colección de escritorios virtuales.<br/>            |
| [**GetExportPath**](getexportpath-win32-rdmsdeploymentsettings.md)                                     | Recupera la ruta de acceso al directorio en el que se implementan las máquinas virtuales para una colección de escritorios virtuales.<br/>                  |
| [**GetInt32Property**](getint32property-win32-rdmsdeploymentsettings.md)                               | Recupera una propiedad de entero para la configuración de implementación de una colección de escritorios virtuales.<br/>                             |
| [**GetSecondaryConnectionString**](win32-rdmsdeploymentsettings-getsecondaryconnectionstring.md)       | Recupera la cadena de conexión secundaria de base de datos de nivel de implementación, que se puede usar para admitir la expiración de contraseña.<br/> |
| [**GetSMBPath**](getsmbpath-win32-rdmsdeploymentsettings.md)                                           | Recupera la ruta de acceso UNC al recurso compartido de SMB en el que se implementan las máquinas virtuales de la colección de escritorios virtuales.<br/>      |
| [**GetStringArrayDeploymentSetting**](getstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | Recupera la configuración de implementación de una colección de escritorios virtuales.<br/>                                                    |
| [**GetStringProperty**](getstringproperty-win32-rdmsdeploymentsettings.md)                             | Recupera una propiedad de cadena para la configuración de implementación de una colección de escritorios virtuales.<br/>                               |
| [**RemoveDeploymentSetting**](removedeploymentsetting-win32-rdmsdeploymentsettings.md)                 | Elimina la configuración de implementación de una colección de escritorios virtuales.<br/>                                                      |
| [**SetBaseVHDPath**](setbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | Recupera la ruta de acceso base al directorio en el que se implementan los VHD de la colección de escritorios virtuales.<br/>                 |
| [**SetConnectionString**](win32-rdmsdeploymentsettings-setconnectionstring.md)                         | Establece la cadena de conexión de base de datos de nivel de implementación.<br/>                                                                  |
| [**SetDiffVHDPath**](setdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | Actualiza la ruta de acceso al directorio en la que se implementan los discos de diferenciación para una colección de escritorios virtuales.<br/>              |
| [**SetExportPath**](setexportpath-win32-rdmsdeploymentsettings.md)                                     | Actualiza la ruta de acceso al directorio en el que se implementan las máquinas virtuales para una colección de escritorios virtuales.<br/>                    |
| [**SetInt32Property**](setint32property-win32-rdmsdeploymentsettings.md)                               | Actualiza una propiedad de entero para la configuración de implementación de una colección de escritorios virtuales.<br/>                               |
| [**SetSecondaryConnectionString**](win32-rdmsdeploymentsettings-setsecondaryconnectionstring.md)       | Establece la cadena de conexión secundaria de base de datos de nivel de implementación.<br/>                                                        |
| [**SetSMBPath**](setsmbpath-win32-rdmsdeploymentsettings.md)                                           | Actualiza la ruta de acceso UNC al recurso compartido de SMB en el que se implementan las máquinas virtuales de la colección de escritorios virtuales.<br/>        |
| [**SetStringArrayDeploymentSetting**](setstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | Actualiza la configuración de implementación de una colección de escritorios virtuales.<br/>                                                      |
| [**SetStringProperty**](setstringproperty-win32-rdmsdeploymentsettings.md)                             | Actualiza una propiedad de cadena para la configuración de implementación de una colección de escritorios virtuales.<br/>                                 |



 

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

 

 





