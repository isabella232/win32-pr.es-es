---
title: MSAD_ReplCursor (clase)
description: Proporciona información de estado de replicación de entrada sobre todas las réplicas de un contexto de nomenclatura determinado (NC).
ms.assetid: 5746cfe9-b113-4be3-b609-15cb937c271b
ms.tgt_platform: multiple
keywords:
- MSAD_ReplCursor clase Active Directory
- Active Directory de MSAD_ReplCursor de clase, se describe
topic_type:
- apiref
api_name:
- MSAD_ReplCursor
- MSAD_ReplCursor.NamingContextDN
- MSAD_ReplCursor.SourceDsaInvocationID
- MSAD_ReplCursor.USNAttributeFilter
- MSAD_ReplCursor.SourceDsaDN
- MSAD_ReplCursor.TimeOfLastSuccessfulSync
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725ac8e9eee9f921ce4109e0b0e42ed85e75ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490738"
---
# <a name="msad_replcursor-class"></a>MSAD \_ ReplCursor (clase)

Proporciona información de estado de replicación de entrada sobre todas las réplicas de un contexto de nomenclatura determinado (NC).

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplCursor
{
  String   NamingContextDN;
  String   SourceDsaInvocationID;
  uint64   USNAttributeFilter;
  String   SourceDsaDN;
  datetime TimeOfLastSuccessfulSync;
};
```

## <a name="members"></a>Miembros

La clase **MSAD \_ ReplCursor** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSAD \_ ReplCursor** tiene estas propiedades.

<dl> <dt>

**NamingContextDN**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene la ruta de acceso X. 500 para el contexto de nomenclatura (NC) que contiene este cursor.

</dd> <dt>

**SourceDsaDN**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la ruta de acceso X. 500 para el agente de sistema de directorio (DSA) que representa el controlador de dominio de origen (DC).

</dd> <dt>

**SourceDsaInvocationID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene el identificador de invocación del servidor de origen al que corresponde el **USNAttributeFilter** .

</dd> <dt>

**TimeOfLastSuccessfulSync**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la marca de tiempo de la última sincronización de replicación correcta con el DSA de origen. Indica la hora a la que este DC vio por última vez los cambios realizados en el DSA de origen para este NC.

</dd> <dt>

**USNAttributeFilter**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el número máximo de secuencias de actualización al que el servidor de destino puede indicar que ha registrado todos los cambios originados por el servidor determinado en números de secuencia de actualización menores o iguales que este número de secuencia de actualización. Esta propiedad se utiliza para filtrar los cambios que el servidor de destino ya ha aplicado en los servidores de origen de replicación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\MicrosoftActiveDirectory raíz<br/>                                               |
| MOF<br/>                      | <dl> <dt>ReplProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_cursor de replicación de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
</dt> </dl>

 

