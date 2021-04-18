---
description: Más información sobre cómo navegar por un árbol de objetos de elemento
ms.assetid: e91f72c8-3ad6-49e8-88cc-aa99c13cd4c2
title: Navegar por un árbol de objetos de elemento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 04e87444c2b9c473268c5e97dd9c26d04d95b93b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715187"
---
# <a name="navigating-a-tree-of-item-objects"></a>Navegar por un árbol de objetos de elemento

> [!Note]  
> Este sistema de scripting se ha reemplazado por el nivel de automatización de adquisición de imágenes de Windows (WIA). Consulte [nivel de automatización de adquisición de imágenes de Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

Una aplicación o un script navega por un árbol de elementos del dispositivo de adquisición de imágenes de Windows (WIA) para buscar y seleccionar imágenes en ese dispositivo. Con esta técnica, una aplicación selecciona y adquiere una imagen sin el uso de un cuadro de diálogo.

Un dispositivo WIA se representa como el elemento raíz en un árbol de objetos de [**elemento**](-wia-item.md) . Los elementos secundarios en el árbol representan carpetas e imágenes para una cámara o escanear camas para un escáner.

Después de conectarse a un dispositivo, llame a la propiedad [**Children**](-wia-iwiadispatchitem-children.md) del objeto de [**elemento**](-wia-item.md) que representa el dispositivo (el elemento raíz del árbol) para obtener una colección de los elementos secundarios (las imágenes o las camas de digitalización) del dispositivo.

Enumerar esta colección (de forma recursiva, si es necesario) para navegar por el árbol de elementos.

 

 
