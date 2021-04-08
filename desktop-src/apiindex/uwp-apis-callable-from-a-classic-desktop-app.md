---
description: La regla general es que una aplicación de escritorio puede llamar a una API de Windows Runtime (WinRT). Sin embargo, algunas API, incluidas las API de la interfaz de usuario XAML, requieren que la aplicación que realiza la llamada tenga una identidad de paquete.
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: API de WinRT que se puede llamar desde una aplicación de escritorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9083fbfb16391c626f49b79176fed7a81068c028
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/24/2020
ms.locfileid: "104078595"
---
# <a name="calling-winrt-apis-from-a-desktop-app"></a>Llamada a las API de WinRT desde una aplicación de escritorio

La regla general es que una aplicación de escritorio puede llamar a una API de WinRT. Sin embargo, algunas API, incluidas las API de la interfaz de usuario XAML, requieren que la aplicación que realiza la llamada tenga una identidad de paquete. Las aplicaciones para UWP tienen un modelo de aplicación bien definido y tienen una identidad de paquete. Los otros tipos de aplicaciones de escritorio no tienen un modelo de aplicación bien definido ni una identidad de paquete. Por lo tanto, si una API requiere una identidad de paquete, una aplicación WPF, Windows Forms o Win32 no puede llamarla a menos que la aplicación [esté empaquetada en un paquete MSIX](/windows/msix/desktop/desktop-to-uwp-root).

## <a name="the-dualapipartition-attribute"></a>El atributo DualApiPartition

Este es el proceso que hay que seguir siempre que haya un WinRT determinado al que le gustaría llamar desde la aplicación de escritorio. Este proceso responderá a la pregunta de si se permite llamar a la API desde una aplicación de escritorio. En primer lugar, visite la referencia de la [API de Windows para Windows Runtime aplicaciones](/uwp/), busque el tema de referencia de la API de clase o miembro que le interese y compruebe si el atributo [**DualApiPartition**](/uwp/api/Windows.Foundation.Metadata.DualApiPartitionAttribute) se encuentra en la sección de atributos.

## <a name="if-the-dualapipartition-attribute-is-listed"></a>Si se muestra el atributo DualApiPartition

Si aparece el atributo DualApiPartition, la API no necesita que la aplicación que realiza la llamada tenga una identidad de paquete y se permite que se llame a la API desde cualquier aplicación de escritorio. [**Windows. Devices. geolocation. geolocator**](/uwp/api/Windows.Devices.Geolocation.Geolocator) es un ejemplo; no es necesario que una aplicación se identifique de forma única para realizar tareas de ubicación.

## <a name="if-the-dualapipartition-attribute-is-not-listed"></a>Si el atributo DualApiPartition no aparece en la lista

Si el atributo DualApiPartition no aparece en la lista, la API necesita que la aplicación que realiza la llamada tenga una identidad de paquete. Por lo tanto, una aplicación de WPF, Windows Forms o Win32 no tiene permiso para llamar a la API a menos que la aplicación se haya convertido en una aplicación de UWP. [**Windows. UI. Xaml. Controls. Button**](/uwp/api/Windows.UI.Xaml.Controls.Button) es un ejemplo.
