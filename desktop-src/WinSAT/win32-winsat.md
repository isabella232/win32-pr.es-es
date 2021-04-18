---
title: Win32_WinSAT (clase)
description: Define la información de evaluación de resumen para la evaluación formal más reciente.
ms.assetid: adf4de42-9dfd-46a7-ae75-3bbcfd15dd68
keywords:
- WinSAT de clase de Win32_WinSAT
- Win32_WinSAT de clase WinSAT, descrito
topic_type:
- apiref
api_name:
- Win32_WinSAT
- Win32_WinSAT.TimeTaken
- Win32_WinSAT.WinSPRLevel
- Win32_WinSAT.WinSATAssessmentState
- Win32_WinSAT.MemoryScore
- Win32_WinSAT.CPUScore
- Win32_WinSAT.DiskScore
- Win32_WinSAT.D3DScore
- Win32_WinSAT.GraphicsScore
api_location:
- WinSATAPI.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829e5e1b3658771728aab9ef30634d90a8bc6450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705187"
---
# <a name="win32_winsat-class"></a>Win32 \_ WinSAT (clase)

\[**Win32 \_** Es posible que WinSAT se modifique o no esté disponible para las versiones después de Windows 8.1.\]

Define la información de evaluación de resumen para la evaluación formal más reciente.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
class Win32_WinSAT
{
  string TimeTaken = "MostRecentAssessment";
  real32 WinSPRLevel;
  uint32 WinSATAssessmentState;
  real32 MemoryScore;
  real32 CPUScore;
  real32 DiskScore;
  real32 D3DScore;
  real32 GraphicsScore;
};
```

## <a name="members"></a>Miembros

La clase de **Win32 \_ WinSAT** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **Win32 \_ WinSAT** tiene estas propiedades.

<dl> <dt>

**CPUScore**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una puntuación para los procesadores del equipo.

</dd> <dt>

**D3DScore**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Después Windows 8.1, WinSAT ya no evaluará las capacidades de los gráficos tridimensionales (juegos) del equipo y la capacidad del controlador de gráficos para representar objetos y ejecutar sombreadores mediante esta evaluación. Por compatibilidad, WinSAT informa de los valores de centinela de las métricas y puntuaciones, pero no se calculan en tiempo real.

</dd> <dt>

**DiskScore**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una puntuación para el rendimiento de lectura secuencial en el disco duro principal del equipo.

</dd> <dt>

**GraphicsScore**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una puntuación para las capacidades de gráficos del equipo.

</dd> <dt>

**MemoryScore**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una puntuación para el rendimiento de la memoria y la capacidad del equipo.

</dd> <dt>

**TimeTaken**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Esta propiedad debe establecerse en "MostRecentAssessment" en la cláusula WHERE de la consulta WQL.

</dd> <dt>

**WinSATAssessmentState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado de la evaluación. Para obtener una descripción de los valores posibles, vea la enumeración [**\_ \_ Estado de evaluación de WINSAT**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) .

<dl> <dt>

<span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**StateUnknown** (0)
</dt> <dt>

<span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Válido** (1)
</dt> <dt>

<span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**IncoherentWithHardware** (2)
</dt> <dt>

<span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**NoAssessmentAvailable** (3)
</dt> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**No válido** (4)
</dt> </dl>

</dd> <dt>

**WinSPRLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Puntuación base del equipo. Para obtener más información sobre el valor de puntuación, vea la propiedad [**IProvideWinSATResultsInfo:: SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para obtener información sobre las puntuaciones de subcomponentes, como **MemoryScore**, vea la propiedad [**IProvideWinSATAssessmentInfo:: score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) .

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo en el que se muestra cómo usar WMI para recuperar datos de esta clase, vea el método [**IProvideWinSATVisuals:: get \_ Bitmap**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WinSAT. mof</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>WinSATAPI.dll</dt> </dl> |



 

 





