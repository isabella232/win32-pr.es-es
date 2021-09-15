---
title: Tipo 1 Complemento de la tienda en línea
description: Tipo 1 Complemento de la tienda en línea
ms.assetid: 3aa74282-522b-4240-8d72-73bd3015abeb
keywords:
- Reproductor de Windows Media en línea, complementos
- tiendas en línea, complementos
- tiendas en línea de tipo 1, complementos
- Reproductor de Windows Media en línea, interfaz IWMPContentPartner
- online stores,IWMPContentPartner (interfaz)
- type 1 online stores,IWMPContentPartner interface
- complementos, Reproductor de Windows Media en línea
- complementos, tiendas en línea
- complementos, escriba 1 tienda en línea
- complementos, interfaz IWMPContentPartner
- Reproductor de Windows Media complementos, escriba 1 tienda en línea
- Reproductor de Windows Media complementos, tiendas en línea
- Reproductor de Windows Media complementos, Reproductor de Windows Media en línea
- Reproductor de Windows Media complementos, interfaz IWMPContentPartner
- IWMPContentPartner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe42095d08262520734603a5418ac6831ce6685
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465823"
---
# <a name="type-1-online-store-plug-in"></a>Tipo 1 Complemento de la tienda en línea

Para aprovechar las características de integración de bibliotecas, los proveedores de tiendas en línea de tipo 1 deben crear un complemento que implemente la [interfaz IWMPContentPartner.](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) Esta interfaz proporciona los métodos que Reproductor de Windows Media para notificar a la tienda en línea las actividades que se están llevando a cabo en el reproductor y para recuperar información específica sobre el contenido de la tienda en línea, el catálogo o la propia tienda.

Después Reproductor de Windows Media crear una instancia del complemento, el reproductor llama a [IWMPContentPartner::SetCallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback)y proporciona un puntero a la interfaz **IWMPContentPartnerCallback.** Esta interfaz proporciona a la tienda en línea una manera de realizar llamadas a Reproductor de Windows Media proporcionar información de estado o iniciar procesos específicos, como descargar una pista de música.

Reproductor de Windows Media y el complemento se ejecutan en procesos independientes. El complemento es un servidor en proceso que se ejecuta en el suplente dll predeterminado, dllhost.exe.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**IWMPContentPartner (interfaz)**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> <dt>

[**IWMPContentPartnerCallback (interfaz)**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)
</dt> </dl>

 

 




