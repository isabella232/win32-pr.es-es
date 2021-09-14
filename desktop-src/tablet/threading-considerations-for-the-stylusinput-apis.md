---
description: Información general sobre las consideraciones de subprocesamiento al usar la interfaz de programación de aplicaciones (API) StylusInput.
ms.assetid: 5d98768a-c60b-4bb0-8640-9bf38254d41f
title: Consideraciones sobre subprocesos para StylusInput API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530ac95fdf0e74e30c83a437b6ed573d03bb2c91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267639"
---
# <a name="threading-considerations-for-the-stylusinput-api"></a>Consideraciones sobre subprocesos para StylusInput API

El [**objeto RealTimeStylus**](realtimestylus-class.md) está diseñado para proporcionar acceso en tiempo real al flujo de datos desde el lápiz de tableta. Complementos, los objetos que implementan la interfaz [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) se pueden agregar a un objeto **RealTimeStylus.** Normalmente, el objeto **RealTimeStylus** llama directamente a los complementos sincrónicos en un subproceso de alta prioridad, mientras que los complementos asincrónicos suelen llamarse en el subproceso de la interfaz de usuario (UI) de la aplicación. Cree o use complementos sincrónicos para las tareas que requieren acceso en tiempo real al flujo de datos y son computacionalmente poco exigentes, como el filtrado de paquetes. Cree o use complementos asincrónicos para tareas que no requieren acceso en tiempo real al flujo de datos, como la colección de lápiz.

Dado que los datos de complemento para la colección asincrónica de complementos del objeto [**RealTimeStylus**](realtimestylus-class.md) están en cola, los complementos asincrónicos pueden recibir datos antes de recibir una llamada a su método [RealTimeStylusDisabled,](/previous-versions/ms824774(v=msdn.10)) pero después de deshabilitar el objeto **RealTimeStylus.** Tenga en cuenta que algunos de los métodos y propiedades del objeto **RealTimeStylus** inician una excepción si el objeto **RealTimeStylus** está deshabilitado.

Los siguientes [**métodos de interfaz IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) pueden llamar a en un subproceso que no sea el subproceso de datos del lápiz de tableta.

-   Se llama a los [métodos RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) y [RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) en el subproceso que actualiza la propiedad [Enabled](/previous-versions/ms585380(v=vs.100)) del objeto [**RealTimeStylus**](realtimestylus-class.md) o que agrega o quita el complemento mientras el objeto **RealTimeStylus está** habilitado.
-   Se [llama al método CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) en el subproceso que llama al método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) del objeto [**RealTimeStylus.**](realtimestylus-class.md)
-   Se [llama](/previous-versions/ms824754(v=msdn.10)) al método Error en el subproceso en el que se ejecuta el complemento sincrónico cuando se produce una excepción.

Para interactuar con la aplicación desde un complemento sincrónico, use el método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) del objeto [**RealTimeStylus**](realtimestylus-class.md) y controle los datos de lápiz óptico personalizados en uno de los complementos asincrónicos. Si realiza una llamada sincrónica a otro subproceso desde un complemento sincrónico, puede bloquear el objeto **RealTimeStylus** y, por tanto, bloquear la colección de entrada de lápiz.

Algunas tareas pueden ser exigentes desde el punto de vista computacional, pero todavía requieren acceso en tiempo real al flujo de datos del lápiz de tableta, como el reconocimiento de gestos multistroke. Las API StylusInput proporcionan un modelo [**RealTimeStylus**](realtimestylus-class.md) en cascada que permite usar dos objetos **RealTimeStylus,** cada uno de los que llaman a sus complementos sincrónicos desde subprocesos diferentes. Para obtener más información sobre el modelo **RealTimeStylus** en cascada, vea [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).

> [!Note]  
> No se puede asociar [**el objeto RealTimeStylus**](realtimestylus-class.md) a una ventana o control en un proceso diferente.

 

Para obtener más información sobre las consideraciones de subprocesamiento para Tablet PC en general, vea Consideraciones sobre [subprocesos de Tablet PC.](tablet-pc-threading-considerations.md)

 

 
