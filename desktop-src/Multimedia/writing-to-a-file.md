---
title: Escribir en un archivo
description: Escribir en un archivo
ms.assetid: a01f93e9-e0fe-4e81-aa9f-62cdca7bce4a
keywords:
- Función AVIFileWriteData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9a6b9a399d8581909c99da615e32ef4487cbb
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372013"
---
# <a name="writing-to-a-file"></a>Escribir en un archivo

Puede escribir información complementaria en un archivo que se ha abierto con privilegios de escritura mediante la [**función AVIFileWriteData.**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) Esta función copia la información de un búfer proporcionado por la aplicación y la coloca en uno o varios fragmentos del archivo. El fragmento "INFO" es un tipo de fragmento RIFF común en el que la función almacena información complementaria. Para obtener una descripción de los archivos RIFF y sus fragmentos de datos, vea [Resource Interchange File Format Services](resource-interchange-file-format-services.md).

 

 




