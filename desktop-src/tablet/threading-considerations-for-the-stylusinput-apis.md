---
description: Información general sobre las consideraciones de subprocesos cuando se usa la interfaz de programación de aplicaciones (API) de StylusInput.
ms.assetid: 5d98768a-c60b-4bb0-8640-9bf38254d41f
title: Consideraciones sobre los subprocesos de la API de StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530ac95fdf0e74e30c83a437b6ed573d03bb2c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103909906"
---
# <a name="threading-considerations-for-the-stylusinput-api"></a>Consideraciones sobre los subprocesos de la API de StylusInput

El objeto [**RealTimeStylus**](realtimestylus-class.md) está diseñado para proporcionar acceso en tiempo real al flujo de datos desde el lápiz de Tablet PC. Los complementos, los objetos que implementan la interfaz [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) se pueden agregar a un objeto **RealTimeStylus** . Los complementos sincrónicos se suelen llamar directamente mediante el objeto **RealTimeStylus** en un subproceso de prioridad alta, mientras que los complementos asincrónicos se suelen llamar en el subproceso de la interfaz de usuario (IU) de la aplicación. Cree o use complementos sincrónicos para tareas que requieran acceso en tiempo real al flujo de datos y que se despidan computacionalmente, como el filtrado de paquetes. Cree o use complementos asincrónicos para tareas que no requieran acceso en tiempo real al flujo de datos, como la colección de entradas de lápiz.

Dado que los datos del complemento de la colección de complementos asincrónicos del objeto [**RealTimeStylus**](realtimestylus-class.md) están en cola, los complementos asincrónicos pueden recibir datos antes de recibir una llamada a su método [RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) , pero después de que el objeto **RealTimeStylus** esté deshabilitado. Tenga en cuenta que algunos de los métodos y propiedades del objeto **RealTimeStylus** producen una excepción si el objeto **RealTimeStylus** está deshabilitado.

Los siguientes métodos de la interfaz [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) pueden llamar a en un subproceso distinto del subproceso de datos del lápiz de Tablet PC.

-   Se llama a los métodos [RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) y [RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) en el subproceso que actualiza la propiedad [Enabled](/previous-versions/ms585380(v=vs.100)) del objeto [**RealTimeStylus**](realtimestylus-class.md) o que agrega o quita el complemento mientras el objeto **RealTimeStylus** está habilitado.
-   Se llama al método [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) en el subproceso que llama al método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) del objeto [**RealTimeStylus**](realtimestylus-class.md) .
-   Se llama al método [error](/previous-versions/ms824754(v=msdn.10)) en el subproceso en el que se ejecuta el complemento sincrónico cuando se produce una excepción.

Para interactuar con la aplicación desde un complemento sincrónico, use el método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) del objeto [**RealTimeStylus**](realtimestylus-class.md) y administre los datos del lápiz personalizado en uno de los complementos asincrónicos. Si realiza una llamada sincrónica a otro subproceso desde un complemento sincrónico, puede bloquear el objeto **RealTimeStylus** y, por lo tanto, bloquear la recopilación de entradas manuscritas.

Es posible que algunas tareas estén exigiendo cálculo todavía, pero que aún requieran acceso en tiempo real al flujo de datos del lápiz de Tablet PC, por ejemplo, para el reconocimiento de gestos de varios trazos. Las API de StylusInput proporcionan un modelo [**RealTimeStylus**](realtimestylus-class.md) en cascada que le permite usar dos objetos **RealTimeStylus** , cada uno de los cuales llama a sus complementos sincrónicos desde subprocesos diferentes. Para obtener más información sobre el modelo **RealTimeStylus** en cascada, vea [el modelo RealTimeStylus en cascada](the-cascaded-realtimestylus-model.md).

> [!Note]  
> No se puede adjuntar el objeto [**RealTimeStylus**](realtimestylus-class.md) a una ventana o control en un proceso diferente.

 

Para obtener más información acerca de las consideraciones de subprocesos para Tablet PC en general, consulte [consideraciones de subprocesos de Tablet PC](tablet-pc-threading-considerations.md)

 

 
