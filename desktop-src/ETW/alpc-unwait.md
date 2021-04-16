---
description: Esta clase es la clase de tipo de evento para eventos de fin de espera de ALPC. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 89a357dd-c217-4b55-994a-4252fa3cae1c
title: ALPC_Unwait (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Unwait
- ALPC_Unwait.Status
api_type:
- NA
api_location: ''
ms.openlocfilehash: f0846eae1ebb88e8892f1fe9b8dd07fd1be9d146
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542766"
---
# <a name="alpc_unwait-class"></a>ALPC ( \_ clase)

Esta clase es la clase de tipo de evento para eventos de fin de espera de ALPC.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(37), EventTypeName("ALPC-Unwait")]
class ALPC_Unwait : ALPC
{
  uint32 Status;
};
```

## <a name="members"></a>Miembros

La clase **ALPC \_ unwait** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **ALPC \_ unwait** tiene estas propiedades.

<dl> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado de la operación de espera.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 




