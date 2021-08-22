---
title: Win32_RDMSManagementData clase
description: Sincroniza los datos de publicación para Escritorio remoto Management Services (RDMS).
ms.assetid: 17f06294-6580-4297-9301-f88314db7775
ms.tgt_platform: multiple
keywords:
- Win32_RDMSManagementData clase Servicios de Escritorio remoto
- Win32_RDMSManagementData clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40c6db0223a18c2fa43de8eed38e670aea36c024f1e66509005bb74f0a8f1cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118849286"
---
# <a name="win32_rdmsmanagementdata-class"></a>Clase \_ RDMSManagementData de Win32

Sincroniza los datos de publicación para Escritorio remoto Management Services (RDMS).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSManagementData
{
};
```

## <a name="members"></a>Miembros

La **clase \_ RDMSManagementData de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **clase \_ RDMSManagementData de Win32** tiene estos métodos.



| Método                                                                                        | Descripción                                                            |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**SynchronizeAllPublishingData**](synchronizeallpublishingdata-win32-rdmsmanagementdata.md) | Sincroniza todos los datos de publicación para RDMS.<br/>                  |
| [**SynchronizePublishingData**](synchronizepublishingdata-win32-rdmsmanagementdata.md)       | Sincroniza el conjunto especificado de datos de publicación para RDMS.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





