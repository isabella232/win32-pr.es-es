---
title: Escribir en un archivo
description: Escribir en un archivo
ms.assetid: a01f93e9-e0fe-4e81-aa9f-62cdca7bce4a
keywords:
- Función AVIFileWriteData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7bf46125d9da8b9e5e0668f504028db8b011c99c780b545f9ea99accc0a9ecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891775"
---
# <a name="writing-to-a-file"></a>Escribir en un archivo

Puede escribir información complementaria en un archivo que se ha abierto con privilegios de escritura mediante la [**función AVIFileWriteData.**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) Esta función copia la información de un búfer proporcionado por la aplicación y la coloca en uno o varios fragmentos del archivo. El fragmento "INFO" es un tipo de fragmento de RIFF común en el que la función almacena información adicional. Para obtener una descripción de los archivos RIFF y sus fragmentos de datos, vea [Resource Interchange File Format Services](resource-interchange-file-format-services.md).

 

 




