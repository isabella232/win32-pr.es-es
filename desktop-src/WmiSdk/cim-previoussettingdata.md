---
description: Asociación entre un sistema virtual y los datos de configuración de la instantánea que es el elemento primario del sistema virtual.
ms.assetid: d11e00e0-a163-49ea-b8ef-e3909a7dc83f
ms.tgt_platform: multiple
title: CIM_PreviousSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PreviousSettingData
- Root\CIMV2.CIM_PreviousSettingData.Target
- Root\CIMV2.CIM_PreviousSettingData.PreviousObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 85f08f22409df8a17bdae33ae81c06cb8167996ecb477f6a2d207d9e0ce2acca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131767"
---
# <a name="cim_previoussettingdata-class"></a>Cim \_ PreviousSettingData (clase)

Asociación entre un sistema virtual y los datos de configuración de la instantánea que es el elemento primario del sistema virtual.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
class CIM_PreviousSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF PreviousObject;
};
```

## <a name="members"></a>Miembros

La **clase \_ CIM PreviousSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM PreviousSettingData** tiene estas propiedades.

<dl> <dt>

**PreviousObject**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ManagedElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Los datos de configuración de instantáneas que son el elemento primario de este sistema de equipo.

</dd> <dt>

**Target**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ManagedElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Sistema informático que era el destino de la aplicación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------|
| Espacio de nombres<br/> | \\CIMV2 raíz<br/> |



 

 




