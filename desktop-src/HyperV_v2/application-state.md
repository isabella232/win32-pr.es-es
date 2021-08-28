---
description: Especifica el estado de mantenimiento de una aplicación.
ms.assetid: CA06AA34-A549-4CFC-9B52-D2E0B200C3E9
title: APPLICATION_STATE enumeración
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPLICATION_STATE
api_type:
- IDLDef
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 5f873e7a30a4cff6dc4cc89eaea225201a367f7c24ead11ad95da04c2ff1ab32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914165"
---
# <a name="application_state-enumeration"></a>ENUMERACIÓN \_ APPLICATION STATE

Especifica el estado de mantenimiento de una aplicación.

## <a name="syntax"></a>Syntax


```C++
typedef enum _APPLICATION_STATE { 
  ApplicationStateHealthy   = 0,
  ApplicationStateCritical
} APPLICATION_STATE, *PAPPLICATION_STATE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**ApplicationStateHealthy**
</dt> <dd>

El estado de la aplicación es correcto.

</dd> <dt>

<span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**ApplicationStateCritical**
</dt> <dd>

El estado de la aplicación es crítico.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para usar este elemento de programación, Windows 8 componentes de integración deben instalarse en la máquina virtual en la que se ejecuta la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                                |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                      |
| Versión<br/>                  | Componentes de integración para Windows 8<br/>                                                           |
| Idl<br/>                      | <dl> <dt>VmApplicationHealthMonitor.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md)
</dt> </dl>

 

 




