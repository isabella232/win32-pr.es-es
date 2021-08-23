---
title: Win32_WinSAT clase
description: Define la información de evaluación de resumen de la evaluación formal más reciente.
ms.assetid: adf4de42-9dfd-46a7-ae75-3bbcfd15dd68
keywords:
- Win32_WinSAT clase WinSAT
- Win32_WinSAT clase WinSAT , descrita
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
ms.openlocfilehash: c0a9e863bd22cebc6609e32521b85de4bca29ae048d9673e3b09cfff2b95408f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504535"
---
# <a name="win32_winsat-class"></a>Win32 \_ WinSAT (clase)

\[**Win32 \_ WinSAT puede** modificarse o no estar disponible para las versiones después de Windows 8.1.\]

Define la información de evaluación de resumen de la evaluación formal más reciente.

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

La **clase \_ WinSAT de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ WinSAT win32** tiene estas propiedades.

<dl> <dt>

**CPUScore**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Puntuación para los procesadores del equipo.

</dd> <dt>

**D3DScore**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Después Windows 8.1, WinSAT ya no evalúa las funcionalidades de gráficos tridimensionales (juegos) del equipo y la capacidad del controlador de gráficos para representar objetos y ejecutar sombreadores mediante esta evaluación. Por compatibilidad, WinSAT informa de los valores de Sentinel para las métricas y puntuaciones, pero estos no se calculan en tiempo real.

</dd> <dt>

**DiskScore**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Puntuación para el rendimiento de lectura secuencial en el disco duro principal del equipo.

</dd> <dt>

**GraphicsScore**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Puntuación de las funcionalidades gráficas del equipo.

</dd> <dt>

**MemoryScore**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Puntuación para el rendimiento de memoria y la capacidad del equipo.

</dd> <dt>

**TimeTaken**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **key**
</dt> </dl>

Esta propiedad debe establecerse en "MostRecentAssessment" en la cláusula WHERE de la consulta WQL.

</dd> <dt>

**WinSATAssessmentState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado de la evaluación. Para obtener una descripción de los valores posibles, vea la [**enumeración WINSAT \_ ASSESSMENT \_ STATE.**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state)

<dl> <dt>

<span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**StateUnknown** (0)
</dt> <dt>

<span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Válido** (1)
</dt> <dt>

<span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**IncoherentWithHardware** (2)
</dt> <dt>

<span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**NoAssessmentAvailable** (3)
</dt> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**No** válido (4)
</dt> </dl>

</dd> <dt>

**WinSPRLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Puntuación base del equipo. Para obtener más información sobre el valor de puntuación, vea la propiedad [**IProvideWinSATResultsInfo::SystemRating.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating)

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para obtener información sobre las puntuaciones de subcomponentes, como **MemoryScore**, vea la propiedad [**IProvideWinSATAssessmentInfo::Score.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo que muestra cómo usar WMI para recuperar datos de esta clase, vea el método [**IProvideWinSATVisuals::get \_ Bitmap.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WinSAT.mof</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>WinSATAPI.dll</dt> </dl> |



 

 





