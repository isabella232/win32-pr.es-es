---
description: Usar propiedades personalizadas.
ms.assetid: 09b30c95-0ce2-401c-a4ae-99c801a2048a
title: Usar propiedades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee01bc0df80acecec9805ea15cd8da65fa23a441c9c7818a88223aa47b963d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813635"
---
# <a name="using-custom-properties"></a>Usar propiedades personalizadas

**Mediante propiedades personalizadas**.

Un Windows adquisición de imágenes (WIA) puede definir sus propias propiedades personalizadas. Los autores de la llamada pueden manipular propiedades personalizadas del mismo modo que lo harían con las propiedades wi-fi normales. Sin embargo, solo la aplicación o el módulo de interfaz de usuario personalizado pueden acceder a estas propiedades personalizadas.

Los controladores WIA deben definir las propiedades personalizadas para que tengan identificadores de propiedad que se desplazan por WIA PRIVATE DEVPROP para las propiedades del dispositivo y usar WIA PRIVATE ITEMPROP para las propiedades de elementos normales, como dentro de \_ \_ \_ \_ [IWiaMiniDrv::d rvInitItemProperties](https://msdn.microsoft.com/library/ms794131.aspx). Para obtener más información, vea [Definir propiedades personalizadas.](-wia-defining-custom-properties.md)

Hay dos maneras de pasar parámetros personalizados a los controladores de WIA.

La primera opción consiste en usar el método **IWiaItemExtras::Escape** (descrito en la documentación del SDK de plataforma). Esto es similar al método [IStiUSD::Escape,](https://msdn.microsoft.com/library/ms794396.aspx) pero permite a los autores de llamadas usar WIA directamente, en lugar de usar métodos DESUSO. Con **IWiaItemExtras::Escape**, puede pasar cualquier información al controlador y el controlador puede devolver cualquier información. El servicio WIA administra solo los búferes pasados entre el autor de la llamada y el controlador.

La segunda opción es usar propiedades personalizadas. El uso del método **IWiaItemExtras::Escape** es más flexible que el uso de propiedades wia personalizadas, pero las propiedades wia personalizadas permiten almacenar información en el flujo de propiedades del elemento para que el controlador pueda leer la información en otro momento.

 

 



