---
title: Generar un cuadro de diálogo para seleccionar formatos restringidos
description: Generar un cuadro de diálogo para seleccionar formatos restringidos
ms.assetid: 486ba928-e06d-4ab0-a642-ba0fe16c8291
keywords:
- Administrador de compresión de audio (ACM), generar cuadros de diálogo
- ACM (Administrador de compresión de audio), generar cuadros de diálogo
- Ejemplos de ACM, generar cuadros de diálogo
- generar cuadros de diálogo
- acmFormatChoose función)
- Administrador de compresión de audio (ACM), seleccionar formatos restringidos
- ACM (Administrador de compresión de audio), seleccionar formatos restringidos
- Ejemplos de ACM, seleccionar formatos restringidos
- selección de formatos restringidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800945f4003c0fbe47d7916e0a1bf707745ff6d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075855"
---
# <a name="producing-a-dialog-box-for-selecting-restricted-formats"></a>Generar un cuadro de diálogo para seleccionar formatos restringidos

Es posible que desee usar el cuadro de diálogo creado por la función [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , pero limite o controle los formatos en el cuadro de diálogo. Para ello, puede usar la marca ACMFORMATCHOOSE \_ STYLEF \_ ENABLEHOOK para enlazar el procedimiento del cuadro de diálogo. A continuación, la aplicación puede filtrar los formatos respondiendo al mensaje [**mm \_ ACM \_ FORMATCHOOSE**](mm-acm-formatchoose.md) en el procedimiento de mensaje para el cuadro de diálogo.

 

 




