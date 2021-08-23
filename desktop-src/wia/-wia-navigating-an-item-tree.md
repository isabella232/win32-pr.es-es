---
description: Una aplicación navega por un Windows de elementos del dispositivo de adquisición de imágenes (WIA) para buscar y seleccionar imágenes en ese dispositivo. Con esta técnica, una aplicación selecciona y adquiere una imagen sin presentar un cuadro de diálogo al usuario.
ms.assetid: 1f124b4a-45fb-4181-b45a-e810a61ac37d
title: Navegar por un árbol de elementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a8ef11fc534a621c31461df897c8cc81f987ef83163a1300b0e392ce4f190e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593025"
---
# <a name="navigating-an-item-tree"></a>Navegar por un árbol de elementos

Una aplicación navega por un Windows de elementos del dispositivo de adquisición de imágenes (WIA) para buscar y seleccionar imágenes en ese dispositivo. Con esta técnica, una aplicación selecciona y adquiere una imagen sin presentar un cuadro de diálogo al usuario.

Un dispositivo WIA se representa como el elemento raíz en un árbol de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) [**o IWiaItem2.**](-wia-iwiaitem2.md) Los elementos secundarios del árbol representan imágenes de una cámara o examen de un escáner.

Una vez seleccionado un dispositivo WIA, una aplicación llama al método [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) de la interfaz [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) del dispositivo para enumerar los elementos secundarios (las imágenes o el examen del dispositivo). Para obtener instrucciones, consulte [Selección de un dispositivo.](-wia-selecting-a-device.md)

El [**método IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) crea un objeto de enumeración para los elementos secundarios del dispositivo y devuelve un puntero a la interfaz [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) de ese objeto. A continuación, la aplicación puede usar los métodos de la **interfaz IEnumWiaItem** para obtener punteros a los elementos del árbol de elementos del dispositivo.

 

 



