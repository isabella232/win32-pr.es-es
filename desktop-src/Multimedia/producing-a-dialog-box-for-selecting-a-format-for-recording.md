---
title: Generar un cuadro de diálogo para seleccionar un formato para la grabación
description: Generar un cuadro de diálogo para seleccionar un formato para la grabación
ms.assetid: e94ca8da-4ee6-4362-a144-27b86f2cadac
keywords:
- Administrador de compresión de audio (ACM), generar cuadros de diálogo
- ACM (administrador de compresión de audio), generar cuadros de diálogo
- Ejemplos de ACM, generar cuadros de diálogo
- generar cuadros de diálogo
- Función acmFormatChoose
- Administrador de compresión de audio (ACM), selección del formato de recoding
- ACM (administrador de compresión de audio), selección del formato de recoding
- Ejemplos de ACM, selección del formato para la recoding
- selección del formato para la recoding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7584d5f56904a6aa5241930041bf89c10373f6b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169537"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-recording"></a>Generar un cuadro de diálogo para seleccionar un formato para la grabación

Una aplicación puede permitir al usuario seleccionar un formato para el que un dispositivo de audio de forma de onda instalado proporciona compatibilidad nativa. Por ejemplo, es posible que desee que un editor de audio de forma de onda grabe nuevos datos de audio de forma de onda sin usar un descomprimidor o un descompresión de ACM para proporcionar una capa de traducción. Para ello, use la función [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) y especifique las marcas \_ ACM FORMATENUMF HARDWARE y ACM FORMATENUMF INPUT en el miembro fdwEnum de la estructura \_ \_ \_ [**ACMFORMATCHOOSE.**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) 

 

 




