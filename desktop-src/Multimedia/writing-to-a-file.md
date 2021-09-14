---
title: Escribir en un archivo
description: Escribir en un archivo
ms.assetid: a01f93e9-e0fe-4e81-aa9f-62cdca7bce4a
keywords:
- Función AVIFileWriteData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9a6b9a399d8581909c99da615e32ef4487cbb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173601"
---
# <a name="writing-to-a-file"></a>Escribir en un archivo

Puede escribir información adicional en un archivo que se ha abierto con privilegios de escritura mediante la [**función AVIFileWriteData.**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) Esta función copia la información de un búfer proporcionado por la aplicación y la coloca en uno o varios fragmentos del archivo. El fragmento "INFO" es un tipo de fragmento de RIFF común en el que la función almacena información adicional. Para obtener una descripción de los archivos RIFF y sus fragmentos de datos, vea [Resource Interchange File Format Services](resource-interchange-file-format-services.md).

 

 




