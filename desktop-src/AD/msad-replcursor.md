---
title: MSAD_ReplCursor clase
description: Proporciona información de estado de replicación entrante sobre todas las réplicas de un contexto de nomenclatura (NC) determinado.
ms.assetid: 5746cfe9-b113-4be3-b609-15cb937c271b
ms.tgt_platform: multiple
keywords:
- MSAD_ReplCursor clase Active Directory
- MSAD_ReplCursor clase Active Directory , descrita
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
ms.openlocfilehash: c001adf774321ba61e232298d070fb4a29d4b3f0740dd8ef900ff4ea0b4cb83a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186070"
---
# <a name="msad_replcursor-class"></a>Clase \_ ReplCursor de MSAD

Proporciona información de estado de replicación entrante sobre todas las réplicas de un contexto de nomenclatura (NC) determinado.

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

La **clase \_ ReplCursor de MSAD** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ReplCursor de MSAD** tiene estas propiedades.

<dl> <dt>

**NamingContextDN**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene la ruta de acceso X.500 para el contexto de nomenclatura (NC) que contiene este cursor.

</dd> <dt>

**SourceDsaDN**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la ruta de acceso X.500 para el agente de sistema de directorios (DSA) que representa el controlador de dominio (DC) de origen.

</dd> <dt>

**SourceDsaInvocationID**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene el identificador de invocación del servidor de origen al que se corresponde **USNAttributeFilter.**

</dd> <dt>

**TimeOfLastSuccessfulSync**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la marca de tiempo de la última sincronización de replicación correcta con la DSA de origen. Indica la hora en que este controlador de dominio vio por última vez los cambios realizados en la DSA de origen para esta controladora de dominio.

</dd> <dt>

**USNAttributeFilter**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el número máximo de secuencia de actualización al que el servidor de destino puede indicar que ha registrado todos los cambios originados por el servidor determinado con números de secuencia de actualización menores o iguales que este número de secuencia de actualización. Esta propiedad se usa para filtrar los cambios que el servidor de destino ya ha aplicado en los servidores de origen de replicación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CURSOR \_ DE REPL de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
</dt> </dl>

 

