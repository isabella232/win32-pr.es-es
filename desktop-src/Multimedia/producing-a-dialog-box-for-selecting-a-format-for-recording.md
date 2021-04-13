---
title: Generar un cuadro de diálogo para seleccionar un formato para la grabación
description: Generar un cuadro de diálogo para seleccionar un formato para la grabación
ms.assetid: e94ca8da-4ee6-4362-a144-27b86f2cadac
keywords:
- Administrador de compresión de audio (ACM), generar cuadros de diálogo
- ACM (Administrador de compresión de audio), generar cuadros de diálogo
- Ejemplos de ACM, generar cuadros de diálogo
- generar cuadros de diálogo
- acmFormatChoose función)
- Administrador de compresión de audio (ACM), seleccionar formato para la recodificación
- ACM (Administrador de compresión de audio), seleccionar formato para la recodificación
- Ejemplos de ACM, seleccionar formato para la recodificación
- selección del formato para la recodificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7584d5f56904a6aa5241930041bf89c10373f6b1
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/27/2020
ms.locfileid: "104420380"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-recording"></a>Generar un cuadro de diálogo para seleccionar un formato para la grabación

Una aplicación puede permitir al usuario seleccionar un formato para el que un dispositivo de audio de forma de onda instalado proporciona compatibilidad nativa. Por ejemplo, podría querer un editor de audio de onda que grabe nuevos datos de audio de onda sin usar un compresor o descompresor de ACM para proporcionar una capa de traducción. Para ello, use la función [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , especificando las marcas de \_ entrada de hardware FORMATENUMF ACM \_ y ACM \_ FORMATENUMF \_ en el miembro **fdwEnum** de la estructura [**acmFormatChoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) .

 

 




