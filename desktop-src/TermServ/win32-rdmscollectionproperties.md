---
title: Win32_RDMSCollectionProperties clase
description: Administra las propiedades de una colección de escritorios virtuales.
ms.assetid: 8c533284-aa7b-4c47-b0a3-33307c4c805b
ms.tgt_platform: multiple
keywords:
- Win32_RDMSCollectionProperties clase Servicios de Escritorio remoto
- Win32_RDMSCollectionProperties clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties
- Win32_RDMSCollectionProperties.Alias
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopMachineName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopHost
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopGuid
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopOsversion
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRamsizeMB
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopArchitecture
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRemoteFX
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopAdapters
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7397ccc1afd350689ac1eeb984a62177140f50
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249735"
---
# <a name="win32_rdmscollectionproperties-class"></a>Clase \_ RDMSCollectionProperties de Win32

Administra las propiedades de una colección de escritorios virtuales.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSCollectionProperties
{
  string  Alias;
  string  ReferenceVirtualDesktopName;
  string  ReferenceVirtualDesktopMachineName;
  string  ReferenceVirtualDesktopHost;
  string  ReferenceVirtualDesktopGuid;
  string  ReferenceVirtualDesktopOsversion;
  uint32  ReferenceVirtualDesktopRamsizeMB;
  string  ReferenceVirtualDesktopArchitecture;
  boolean ReferenceVirtualDesktopRemoteFX = false;
  string  ReferenceVirtualDesktopAdapters[];
};
```

## <a name="members"></a>Members

La **clase \_ RDMSCollectionProperties de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](/windows)

### <a name="methods"></a>Métodos

La **clase \_ RDMSCollectionProperties de Win32** tiene estos métodos.



| Método                                                                                        | Descripción                                                                         |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**GetProvisioningProperties**](getprovisioningproperties-win32-rdmscollectionproperties.md) | Recupera las propiedades de aprovisionamiento de la colección de escritorios virtuales.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ RDMSCollectionProperties de Win32** tiene estas propiedades.

<dl> <dt>

**Alias**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene el alias de la colección.

</dd> <dt>

**ReferenceVirtualDesktopAdapters**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece los nombres de los adaptadores de red virtual de la máquina virtual maestra.

</dd> <dt>

**ReferenceVirtualDesktopArchitecture**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece la arquitectura del procesador de la máquina virtual maestra.

</dd> <dt>

**ReferenceVirtualDesktopGuid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece el GUID de la máquina virtual maestra.

</dd> <dt>

**ReferenceVirtualDesktopHost**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece el nombre del servidor host de la máquina virtual maestra.

</dd> <dt>

**ReferenceVirtualDesktopMachineName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece el nombre de la máquina virtual maestra.

</dd> <dt>

**ReferenceVirtualDesktopName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece el nombre de la máquina virtual maestra.

</dd> <dt>

**ReferenceVirtualDesktopOsversion**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece la versión del sistema operativo de la máquina virtual maestra.

</dd> <dt>

**ReferenceVirtualDesktopRamsizeMB**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece el tamaño de memoria de la máquina virtual maestra.

</dd> <dt>

**ReferenceVirtualDesktopRemoteFX**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece un valor que indica si RemoteFX está habilitado para la máquina virtual maestra. **TRUE** si RemoteFX está habilitado; de lo contrario, **FALSE**. El valor predeterminado de esta propiedad es **FALSE.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | Rdms \\ cimv2 \\ raíz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Escritorio remoto Management Services Provider](rdms-api-reference.md)
</dt> </dl>

 

