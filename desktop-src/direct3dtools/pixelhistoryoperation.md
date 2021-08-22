---
description: Representa información sobre el historial de píxeles.
MS-HAID: vspixengine.PixelHistoryOperation
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura PixelHistoryOperation
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59DC72FC-3865-48D3-9F92-9BE93DCA093B
api_name:
- PixelHistoryOperation
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 15cae4986b7dc109c08011d2cc23e1b6133de9e5
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625191"
---
# <a name="span-idvspixenginepixelhistoryoperationspanpixelhistoryoperation-structure"></a><span id="vspixengine.pixelhistoryoperation"></span>Estructura PixelHistoryOperation

Representa información sobre el historial de píxeles.

## <a name="syntax"></a>Sintaxis


```C++
} PixelHistoryOperation;
```

## <a name="members"></a>Miembros

**Eid**  
Identificador del evento gráfico asociado a esta operación.

**PCP**  
Llamadas empaquetadas asociadas a esta operación.

**renderTargetPtr**  
Destino de representación asociado originalmente (dentro de la aplicación capturada) a esta operación.

**iPrim**  
Índice de la primitiva real asociada a su operación.

**numPrims**  
Número total de primitivas asociadas a esta operación.

**numVertsPerPrim**  
Número de vértices por primitiva.

**iInstance**  
Al representar instancias, el número de instancia de la instancia real asociada a esta operación.

**iInstanceCount**  
Al representar instancias, el número total de instancias asociadas a esta operación.

**bAssemblerStageGeneratesInstanceID**  
true si el ensamblador de entrada genera los iDs de instancia; en caso contrario, false.

**flags**  
Combinación de valores PIXELHISTORYFLAGS. Para obtener más información, vea la enumeración PIXELHISTORYFLAGS.

**pVSFile**  
FILEPTR para el flujo de bytes del sombreador de píxeles. Esto se pasa de nuevo para depurar.

**pGSFile**  
FILEPTR para el flujo de bytes del sombreador de geometría. Esto se pasa de nuevo para depurar.

**pPSFile**  
FILEPTR para el flujo de bytes del sombreador de píxeles. Esto se pasa de nuevo para depurar.

**pHSFile**  
FILEPTR para el flujo de bytes del sombreador de casco. Esto se pasa de nuevo para depurar.

**pDSFile**  
FILEPTR para el flujo de bytes del sombreador de dominio. Esto se pasa de nuevo para depurar.

**pCSFile**  
FILEPTR para el flujo de bytes del sombreador de proceso. Esto se pasa de nuevo para depurar.

**VertexShaderFile**  
Cadena COM que contiene la ruta de archivo del archivo de origen del sombreador de vértices.

**PixelShaderFile**  
Cadena COM que contiene la ruta de archivo del archivo de origen del sombreador de píxeles.

**GeometryShaderFile**  
Cadena COM que contiene la ruta de archivo del archivo de origen del sombreador de geometría.

**HullShaderFile**  
Cadena COM que contiene la ruta de archivo del archivo de origen del sombreador de casco.

**DomainShaderFile**  
Cadena COM que contiene la ruta de archivo del archivo de origen del sombreador de dominio.

**psRed**  
Salida del sombreador de píxeles: valor del componente de color rojo.

**psGreen**  
Salida del sombreador de píxeles: valor del componente de color verde.

**psBlue**  
Salida del sombreador de píxeles: valor del componente de color azul

**psAlpha**  
Salida del sombreador de píxeles: valor del componente de color alfa

**LabelPSRed**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color rojo de la salida del sombreador de píxeles.

**LabelPSGreen**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color verde de la salida del sombreador de píxeles.

**LabelPSBlue**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color azul de la salida del sombreador de píxeles.

**LabelPSAlpha**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color alfa de la salida del sombreador de píxeles.

**pixelKillReason**  
Salida del sombreador de píxeles: motivo por el que se ha detenido la salida de píxeles.

**pixelOccluded**  
true si el píxel está ocluido; de lo contrario, false.

**fbRed**  
Framebuffer: valor del componente de color rojo del búfer de fotogramas antes de combinar la salida del sombreador de píxeles.

**fbGreen**  
Framebuffer: valor del componente de color verde del búfer de fotogramas antes de combinar la salida del sombreador de píxeles.

**fbBlue**  
Framebuffer: valor del componente de color azul del búfer de fotogramas antes de combinar la salida del sombreador de píxeles.

**fbAlpha**  
Framebuffer: valor del componente de color alfa del búfer de fotogramas antes de combinar la salida del sombreador de píxeles.

**LabelFBRed**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color rojo del búfer de fotogramas.

**LabelFBGreen**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color verde del búfer de fotogramas.

**LabelFBBlue**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color azul del búfer de fotogramas.

**LabelFBAlpha**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color alfa del búfer de fotogramas.

**Topología**  
Topología de vértices de las llamadas a draw (lista de triángulos, franja de triángulo, etc.).

**Vértices**  
Cadena COM que contiene el búfer de vértices a partir de esta primitiva. El búfer de vértices sigue el formato de diseño de entrada especificado en la fase de canalización.

**vertexSize**  
Tamaño de un solo vértice en bytes.

**InputLayout**  
Cadena COM que contiene una secuencia de estructuras InputLayoutStruct asociadas a la llamada a draw.

**Hresult**  
The DirectX Hresult. En caso de un problema, se puede usar para mostrar el error.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



