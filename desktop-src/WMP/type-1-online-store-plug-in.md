---
title: Escriba 1 complemento de tienda en línea
description: Escriba 1 complemento de tienda en línea
ms.assetid: 3aa74282-522b-4240-8d72-73bd3015abeb
keywords:
- Windows Media Player tiendas en línea, Complementos
- tiendas en línea, Complementos
- tipo 1 tiendas en línea, Complementos
- Windows Media Player tiendas en línea, interfaz IWMPContentPartner
- tiendas en línea, interfaz IWMPContentPartner
- tipo 1 tiendas en línea, interfaz IWMPContentPartner
- complementos, Windows Media Player tiendas en línea
- complementos, tiendas en línea
- complementos, escriba 1 tiendas en línea
- complementos, interfaz IWMPContentPartner
- Complementos de Windows Media Player, escriba 1 tiendas en línea
- Complementos de Windows Media Player, tiendas en línea
- Complementos de Windows Media Player, Windows Media Player tiendas en línea
- Complementos de Media Player de Windows, interfaz IWMPContentPartner
- IWMPContentPartner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe42095d08262520734603a5418ac6831ce6685
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104077452"
---
# <a name="type-1-online-store-plug-in"></a>Escriba 1 complemento de tienda en línea

Para aprovechar las características de integración de bibliotecas, escriba 1 los proveedores de tiendas en línea deben crear un complemento que implemente la interfaz [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) . Esta interfaz proporciona los métodos que Windows Media Player llama para notificar a la tienda en línea sobre las actividades que se realizan en el reproductor y para recuperar información específica sobre el contenido de la tienda en línea, el catálogo o el propio almacén.

Una vez que Windows Media Player crea instancias del complemento, el reproductor llama a [IWMPContentPartner:: SetCallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback)y proporciona un puntero a la interfaz **IWMPContentPartnerCallback** . Esta interfaz proporciona a la tienda en línea una forma de realizar llamadas en Media Player de Windows para proporcionar información de estado o para iniciar procesos específicos, como la descarga de una pista de música.

Windows Media Player y el complemento se ejecutan en procesos independientes. El complemento es un servidor en proceso que se ejecuta en el suplente de DLL predeterminado, dllhost.exe.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Interfaz IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> <dt>

[**Interfaz IWMPContentPartnerCallback**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)
</dt> </dl>

 

 




