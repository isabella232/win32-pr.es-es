---
description: Una aplicación navega por un árbol de elementos del dispositivo de adquisición de imágenes de Windows (WIA) para buscar y seleccionar imágenes en ese dispositivo. Con esta técnica, una aplicación selecciona y adquiere una imagen sin presentar un cuadro de diálogo al usuario.
ms.assetid: 1f124b4a-45fb-4181-b45a-e810a61ac37d
title: Navegar por un árbol de elementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787ff3b53690ae7db4ff69fd5de2f4f4186f8e43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541934"
---
# <a name="navigating-an-item-tree"></a>Navegar por un árbol de elementos

Una aplicación navega por un árbol de elementos del dispositivo de adquisición de imágenes de Windows (WIA) para buscar y seleccionar imágenes en ese dispositivo. Con esta técnica, una aplicación selecciona y adquiere una imagen sin presentar un cuadro de diálogo al usuario.

Un dispositivo WIA se representa como el elemento raíz en un árbol de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) . Los elementos secundarios del árbol representan las imágenes de una cámara o escanean las camas de un escáner.

Una vez que se selecciona un dispositivo WIA, una aplicación llama al método [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) de la interfaz [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) del dispositivo para enumerar los elementos secundarios (las imágenes o las camas de digitalización) del dispositivo. Para obtener instrucciones, consulte [seleccionar un dispositivo](-wia-selecting-a-device.md).

El método [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) crea un objeto de enumeración para los elementos secundarios del dispositivo y devuelve un puntero a la interfaz [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) de ese objeto. A continuación, la aplicación puede usar los métodos de la interfaz **IEnumWiaItem** para obtener punteros a los elementos del árbol de elementos del dispositivo.

 

 



