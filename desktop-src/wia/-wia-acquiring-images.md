---
description: Una vez que se ha seleccionado una imagen, una aplicación usa la interfaz IWiaDataTransfer (para aplicaciones que se ejecutan en Windows XP o versiones anteriores) o la interfaz IWiaTransfer (para aplicaciones que se ejecutan en Windows Vista o posterior) para transferir datos de imagen desde dispositivos de imágenes. Vea transferir datos de imagen en WIA 1,0 o transferir datos de imagen en WIA 2,0 para obtener más información.
ms.assetid: cf76e526-d63b-4ee5-ba3c-871f2051a82c
title: Adquirir imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d062cb370327311ad0c7d4f883344c05bb776f6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697186"
---
# <a name="acquiring-images"></a>Adquirir imágenes

Una vez que se ha seleccionado una imagen, una aplicación usa la interfaz [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) (para aplicaciones que se ejecutan en Windows XP o versiones anteriores) o la interfaz [**IWiaTransfer**](-wia-iwiatransfer.md) (para aplicaciones que se ejecutan en Windows Vista o posterior) para transferir datos de imagen desde dispositivos de imágenes. Vea [transferir datos de imagen en wia 1,0](-wia-transferring-image-data.md) o transferir [datos de imagen en WIA 2,0](-wia-transferring-image-data-in-wia2.md) para obtener más información.

Una vez que se ha seleccionado un dispositivo, una aplicación usa el método [**IWiaItem::D evicedlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) de la interfaz [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) del dispositivo (el elemento raíz) para seleccionar una imagen de un dispositivo de adquisición de imágenes de Windows (WIA) especificado. El método [**IWiaDevMgr:: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) muestra un cuadro de diálogo que permite al usuario seleccionar una imagen de un dispositivo especificado y transfiere la imagen a un nombre de archivo seleccionado por el usuario. También permite al usuario especificar un dispositivo si es necesario. Para obtener más información, consulte [seleccionar un dispositivo](-wia-selecting-a-device.md) .

Tenga en cuenta que no es necesario que un usuario seleccione una imagen con el método anterior. Una aplicación puede obtener un puntero a un elemento de imagen directamente desde el árbol de elementos de un dispositivo. Para obtener instrucciones, consulte [navegar por un árbol de elementos](-wia-navigating-an-item-tree.md).

Una vez que se ha seleccionado el elemento WIA que representa la imagen deseada, una aplicación que se ejecuta en Windows XP o anterior consulta la interfaz [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) de ese elemento para un puntero a su interfaz [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) . Una aplicación que se ejecuta en Windows Vista o posterior consulta la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) para un puntero a su interfaz [**IWiaTransfer**](-wia-iwiatransfer.md) .

A continuación, la aplicación puede usar los métodos de la interfaz [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) (o [**IWiaTransfer**](-wia-iwiatransfer.md)) para transferir los datos de la imagen a la aplicación.

Si el dispositivo de creación de imágenes es un escáner, [**IWiaDataTransfer:: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata)u otros métodos de la interfaz [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) , desencadena una operación de análisis y, a continuación, transfiere los datos de la imagen resultante. Si el dispositivo es una cámara, los datos de la imagen se transfieren simplemente de la cámara a la aplicación.

 

 



