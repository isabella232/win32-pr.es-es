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
ms.openlocfilehash: 800945f4003c0fbe47d7916e0a1bf707745ff6d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169530"
---
# <a name="producing-a-dialog-box-for-selecting-restricted-formats"></a>Generar un cuadro de diálogo para seleccionar formatos restringidos

Es posible que quiera usar el cuadro de diálogo creado por la función [**acmFormatChoose,**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) pero limitar o controlar los formatos del cuadro de diálogo. Para ello, use la marca ACMFORMATCHOOSE \_ STYLEF \_ ENABLEHOOK para enlazar el procedimiento de diálogo. A continuación, la aplicación puede filtrar los formatos respondiendo al mensaje [**\_ \_ FORMATCHOOSE**](mm-acm-formatchoose.md) de MM ACM en el procedimiento de mensaje del cuadro de diálogo.

 

 




