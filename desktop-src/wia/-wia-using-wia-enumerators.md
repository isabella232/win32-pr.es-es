---
description: WIA proporciona varias interfaces para enumerar diversas funcionalidades, propiedades e información.
ms.assetid: d46d4c18-79cc-4f3c-9745-522ab2635068
title: Usar enumeradores WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ee42f99718cb36071b828e87e3a71de6d70ab5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275451"
---
# <a name="using-wia-enumerators"></a>Usar enumeradores WIA

WIA proporciona varias interfaces para enumerar diversas funcionalidades, propiedades e información. Las interfaces de enumeración de adquisición de imágenes de Windows (WIA) son implementaciones específicas de la interfaz de enumeración del modelo de objetos componentes (COM) estándar. Para obtener más información, consulte [IEnumXXXX](/previous-versions//ms680089(v=vs.85)).

En la tabla siguiente se proporciona información sobre las interfaces de enumeración de WIA. 

| Interfaz                                                   | Cómo obtener un puntero                                                                                                                                                                                    | Se usa para                                                                                                                             |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWIA \_ dev \_ caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)       | Llame a un método [**IWiaItem:: EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) o [**IWiaItem2:: EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) de un elemento de la raíz de WIA. | Enumera las capacidades de un dispositivo de hardware WIA, como comandos y eventos de dispositivo.                                            |
| [**\_Información de desarrollo de IEnumWIA \_**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)       | Llame al método [**IWiaDevMgr:: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) o [**IWiaDevMgr2:: EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md) .                                            | Enumera los dispositivos WIA disponibles y proporciona punteros a sus interfaces [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) . |
| [**\_Información de formato de IEnumWIA \_**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) | Llame a un método de [**\_ \_ información de formato IWiaDataTransfer:: idtEnumWIA**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtenumwia_format_info) de un elemento.                                                                              | Enumera toda la información de formato de imagen que proporciona un elemento WIA.                                                                    |
| [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem)                   | Llame a un método [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) o [**IWiaItem2:: ENUMCHILDITEMS**](-wia-iwiaitem2-enumchilditems.md) de elemento WIA.                                          | Enumera los elementos secundarios de un elemento WIA que representa un dispositivo o una carpeta.                                                |



 

 

 
