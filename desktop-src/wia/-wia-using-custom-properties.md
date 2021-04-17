---
description: Usar propiedades personalizadas.
ms.assetid: 09b30c95-0ce2-401c-a4ae-99c801a2048a
title: Usar propiedades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca9f8092afa5b8af22080b154fff79a32a6f304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696504"
---
# <a name="using-custom-properties"></a>Usar propiedades personalizadas

**Usar propiedades personalizadas**.

Un controlador de adquisición de imágenes de Windows (WIA) puede definir sus propias propiedades personalizadas. Los llamadores pueden manipular propiedades personalizadas del mismo modo que las propiedades de WIA normales. Sin embargo, solo el módulo de la aplicación o de la interfaz de usuario personalizada puede tener acceso a estas propiedades personalizadas.

Los controladores WIA deben definir las propiedades personalizadas para tener identificadores de propiedad que se desplacen con WIA \_ Private \_ DEVPROP para las propiedades de dispositivo y usar WIA \_ Private \_ ITEMPROP para las propiedades de elementos normales, como dentro de [IWiaMiniDrv::d rvinititemproperties](https://msdn.microsoft.com/library/ms794131.aspx). Para obtener más información, vea [definir propiedades personalizadas](-wia-defining-custom-properties.md).

Hay dos maneras de pasar parámetros personalizados a los controladores WIA.

La primera opción consiste en usar el método **IWiaItemExtras:: escape** (descrito en la documentación del SDK de la plataforma). Esto es similar al método [IStiUSD:: escape](https://msdn.microsoft.com/library/ms794396.aspx) , pero permite que los llamadores usen WIA directamente, en lugar de usar métodos STI. Con **IWiaItemExtras:: escape**, puede pasar cualquier información al controlador y el controlador puede devolver cualquier información. El servicio WIA solo administra los búferes pasados entre el autor de la llamada y el controlador.

La segunda opción consiste en usar las propiedades personalizadas. Usar el método **IWiaItemExtras:: escape** es más flexible que usar las propiedades de WIA personalizadas, pero las propiedades de WIA personalizadas permiten almacenar información en el flujo de propiedades del elemento para que el controlador pueda leer la información en otro momento.

 

 



