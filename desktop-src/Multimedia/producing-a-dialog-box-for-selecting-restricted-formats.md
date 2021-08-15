---
title: Generar un cuadro de diálogo para seleccionar formatos restringidos
description: Generar un cuadro de diálogo para seleccionar formatos restringidos
ms.assetid: 486ba928-e06d-4ab0-a642-ba0fe16c8291
keywords:
- Administrador de compresión de audio (ACM), generar cuadros de diálogo
- ACM (administrador de compresión de audio), generar cuadros de diálogo
- Ejemplos de ACM, generar cuadros de diálogo
- generar cuadros de diálogo
- Función acmFormatChoose
- Administrador de compresión de audio (ACM), selección de formatos restringidos
- ACM (administrador de compresión de audio), selección de formatos restringidos
- Ejemplos de ACM, selección de formatos restringidos
- seleccionar formatos restringidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994fffa7ef13f6febe41eb766b4ecaef7eb735f11f58d36f37adfccbb152bffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802045"
---
# <a name="producing-a-dialog-box-for-selecting-restricted-formats"></a>Generar un cuadro de diálogo para seleccionar formatos restringidos

Es posible que quiera usar el cuadro de diálogo creado por la función [**acmFormatChoose,**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) pero limitar o controlar los formatos en el cuadro de diálogo. Para ello, use la marca ACMFORMATCHOOSE \_ STYLEF \_ ENABLEHOOK para enlazar el procedimiento de diálogo. A continuación, la aplicación puede filtrar los formatos respondiendo al mensaje [**MM \_ ACM \_ FORMATCHOOSE en**](mm-acm-formatchoose.md) el procedimiento de mensaje del cuadro de diálogo.

 

 




