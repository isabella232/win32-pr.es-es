---
description: Un contexto de dispositivo primario permite a una aplicación minimizar el tiempo necesario para configurar la región de recorte de una ventana.
ms.assetid: 194d5add-d1a1-4c10-89ee-171ff008a7ab
title: Contextos de dispositivo de pantalla primaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e423ceaa65790df35fa55c8dda597cb1bb45019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984882"
---
# <a name="parent-display-device-contexts"></a>Contextos de dispositivo de pantalla primaria

Un *contexto de dispositivo primario* permite a una aplicación minimizar el tiempo necesario para configurar la región de recorte de una ventana. Normalmente, una aplicación usa contextos de dispositivo primarios para acelerar el dibujo de ventanas de control sin necesidad de un contexto de dispositivo privado o de clase. Por ejemplo, el sistema utiliza contextos de dispositivo primarios para los controles de botón de control y edición. Los contextos de dispositivos primarios están pensados para usarse solo con ventanas secundarias, nunca con ventanas emergentes o de nivel superior.

Una aplicación puede especificar el \_ estilo CS PARENTDC para establecer la región de recorte de la ventana secundaria en la de la ventana primaria para que el elemento secundario pueda dibujar en el elemento primario. Al especificar CS \_ PARENTDC, se mejora el rendimiento de una aplicación porque no es necesario que el sistema siga recalculando el área visible para cada ventana secundaria.

Los valores de atributo establecidos por la ventana primaria no se conservan para la ventana secundaria; por ejemplo, la ventana primaria no puede establecer el pincel para sus ventanas secundarias. La única propiedad conservada es la región de recorte. La ventana debe recortar su propia salida a los límites de la ventana. Dado que la región de recorte del contexto del dispositivo primario es idéntica a la ventana primaria, la ventana secundaria podría dibujarse en toda la ventana primaria, pero el contexto del dispositivo primario no debe usarse de esta manera.

El sistema omite el estilo CS \_ PARENTDC si la ventana primaria usa un contexto de dispositivo privado o de clase, si la ventana primaria recorta sus ventanas secundarias, o si la ventana secundaria recorta sus ventanas secundarias o las ventanas del mismo nivel.

 

 



