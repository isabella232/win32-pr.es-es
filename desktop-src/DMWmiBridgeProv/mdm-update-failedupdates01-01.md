---
title: MDM_Update_FailedUpdates01_01 (clase)
description: La \_ clase de actualización \_ FailedUpdates01 01 de MDM \_ se utiliza para administrar las actualizaciones con errores.
ms.assetid: 3bb7993b-b44b-44d1-84ee-dbdda0093ca0
keywords:
- MDM_Update_FailedUpdates01_01 (clase)
- MDM_Update_FailedUpdates01_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Update_FailedUpdates01_01
- MDM_Update_FailedUpdates01_01.InstanceID
- MDM_Update_FailedUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0ba8d42d97b15cd195e87f536abad9610492e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489166"
---
# <a name="mdm_update_failedupdates01_01-class"></a>\_ \_ Clase FailedUpdates01 01 de actualización \_ de MDM

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La clase de **\_ actualización \_ FailedUpdates01 \_ 01 de MDM** se utiliza para administrar las actualizaciones con errores.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_FailedUpdates01_01
{
  string InstanceID;
  string ParentID;
  sint32 HResult;
  sint32 State;
};
```

## <a name="members"></a>Miembros

La clase de **\_ actualización \_ FailedUpdates01 \_ 01 de MDM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ actualización \_ FailedUpdates01 \_ 01 de MDM** tiene estas propiedades.

<dl> <dt>

[HResult](/windows/client-management/mdm/update-csp#failedupdates-failed-update-guid-hresult)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica el nombre del nodo primario. Para esta clase, la cadena es el GUID de la actualización con errores.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/Update/FailedUpdates".

</dd> <dt>

[**State**](/windows/client-management/mdm/update-csp)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                            |
| Espacio de nombres<br/>                | Dmmap de MDM raíz de \\ cimv2 \\ \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl>      |
| Archivo DLL<br/>                      | <dl> <dt>\\DMWmiBridgeProv.dllMOF</dt> </dl> |



 

