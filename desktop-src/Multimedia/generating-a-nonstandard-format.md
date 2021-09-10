---
title: Generar un formato no estándar
description: Generar un formato no estándar
ms.assetid: e9f80aec-d5dc-4c44-aea0-95220542e48d
keywords:
- Administrador de compresión de audio (ACM), formatos no estándar
- ACM (administrador de compresión de audio), formatos no estándar
- Ejemplos de ACM, formatos no estándar
- Función acmFormatSuggest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e775fb09f926e0380b8141101b816b0dcbb221
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370345"
---
# <a name="generating-a-nonstandard-format"></a>Generar un formato no estándar

A veces, una aplicación necesita un formato no estándar. Por ejemplo, una aplicación podría necesitar un archivo de formato ADPCM de 16 kHz. Dado que 16 kHz no es estándar, las funciones de enumeración no generarán este formato. De hecho, a falta de codificar de forma personalizada los algoritmos de formato en la aplicación, no hay ninguna manera confiable de generar un formato no estándar. Sin embargo, a veces es posible generar un formato análogo configurando un formato PCM válido con toda la información necesaria y, a continuación, usando la [**función acmFormatSuggest.**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) Dado que los descomprimores y los descompresión intentan sugerir un formato más cercano al formato deseado, el número de canales y la frecuencia se conservan normalmente.

 

 




