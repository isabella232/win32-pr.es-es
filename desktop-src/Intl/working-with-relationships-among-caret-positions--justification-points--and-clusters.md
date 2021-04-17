---
description: En la tabla siguiente se muestran los distintos métodos que la aplicación puede utilizar para controlar el símbolo de intercalación, la justificación y los clústeres.
ms.assetid: 950a24b4-62ab-4eaf-ac15-87434d3c28c0
title: Trabajar con relaciones entre posiciones del símbolo de intercalación, puntos de justificación y clústeres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d051d008a8ae991b2858be598713fe9ad1adc0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686814"
---
# <a name="working-with-relationships-among-caret-positions-justification-points-and-clusters"></a>Trabajar con relaciones entre posiciones del símbolo de intercalación, puntos de justificación y clústeres

En la tabla siguiente se muestran los distintos métodos que la aplicación puede utilizar para controlar el símbolo de intercalación, la justificación y los clústeres.



| Tarea                             | Compatibilidad con Uniscribe                                                                                                                                                                                                                                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Símbolo de intercalación movimiento por clúster de caracteres  | El parámetro *pwLogClust* del miembro [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** de la estructura [**\_ VISATTR del script**](/windows/win32/api/usp10/ns-usp10-script_visattr) .<br/> El miembro **fCharStop** de la [**estructura \_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr)<br/> |
| Salto de línea entre caracteres | El parámetro *pwLogClust* del miembro [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** de la estructura [**\_ VISATTR del script**](/windows/win32/api/usp10/ns-usp10-script_visattr) .<br/> El miembro **fCharStop** de la [**estructura \_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr)<br/> |
| Movimiento de intercalación por palabra               | El miembro **fWordStop** de la [**estructura \_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr)                                                                                                                                                                                            |
| División de líneas entre palabras      | El miembro **fWordStop** de la [**estructura \_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr)                                                                                                                                                                                            |
| Justificación                    | El miembro **uJustification** de la [**estructura \_ VISATTR de script**](/windows/win32/api/usp10/ns-usp10-script_visattr)                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




