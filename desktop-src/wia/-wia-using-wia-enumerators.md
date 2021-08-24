---
description: WIA proporciona varias interfaces para enumerar varias funcionalidades, propiedades e información.
ms.assetid: d46d4c18-79cc-4f3c-9745-522ab2635068
title: Uso de enumeradores WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47b6e822d38c73171767d43afd416d09648bd6b82095b9408e2f17827751b0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813475"
---
# <a name="using-wia-enumerators"></a>Uso de enumeradores WIA

WIA proporciona varias interfaces para enumerar varias funcionalidades, propiedades e información. Las Windows de enumeración de adquisición de imágenes de componentes (WIA) son todas implementaciones específicas de la interfaz de enumeración del Modelo de objetos componentes (COM) estándar. Para obtener más información, [vea IEnumXXXX](/previous-versions//ms680089(v=vs.85)).

En la tabla siguiente se proporciona información sobre las interfaces de enumeración de WIA. 

| Interfaz                                                   | Cómo obtener un puntero                                                                                                                                                                                    | Se usa para                                                                                                                             |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**CAPS de \_ DESARROLLO de IEnumWIA \_**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)       | Llame a [**un método IWiaItem::EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) o [**IWiaItem2::EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) de un elemento raíz de WIA. | Enumera las funcionalidades de un dispositivo de hardware WIA, como los comandos y eventos del dispositivo.                                            |
| [**IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)       | Llame al [**método IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) o [**IWiaDevMgr2::EnumDeviceInfo.**](-wia-iwiadevmgr2-enumdeviceinfo.md)                                            | Enumera los dispositivos WIA disponibles y proporciona punteros a sus [**interfaces IWiaPropertyStorage.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) |
| [**IEnumWIA \_ FORMAT \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) | Llame a [**un método IWiaDataTransfer::idtEnumWIA \_ FORMAT \_ INFO**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtenumwia_format_info) de un elemento.                                                                              | Enumera toda la información de formato de imagen que proporciona un elemento de WIA.                                                                    |
| [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem)                   | Llame a [**un método IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) o [**IWiaItem2::EnumChildItems**](-wia-iwiaitem2-enumchilditems.md) del elemento WIA.                                          | Enumera los elementos secundarios de un elemento de WIA que representa un dispositivo o una carpeta.                                                |



 

 

 
