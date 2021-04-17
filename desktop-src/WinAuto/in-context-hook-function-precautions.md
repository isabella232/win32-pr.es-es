---
title: Precauciones de la función de enlace de In-Context
description: Por motivos de rendimiento, los desarrolladores de cliente registran funciones de enlace en contexto.
ms.assetid: 14b48920-a291-4519-b005-e559263a0e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c0e319037cb1295725548b3361bf076b4b1f760
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714415"
---
# <a name="in-context-hook-function-precautions"></a>Precauciones de la función de enlace de In-Context

Por motivos de rendimiento, los desarrolladores de cliente registran funciones de enlace en contexto. Sin embargo, dado que estas funciones de enlace están asignadas en el espacio de direcciones del servidor, los desarrolladores de cliente y servidor deben tomar precauciones para asegurarse de que el procesamiento de eventos se realiza sin problemas.

## <a name="precautions-for-client-developers"></a>Precauciones para los desarrolladores de cliente

Los desarrolladores de cliente deben tener en cuenta los siguientes problemas:

-   Las funciones de enlace en contexto no deben usar mucho tiempo de procesador, ya que la función de enlace debe devolver antes de que continúe la aplicación de servidor.
-   Después de desencadenar un evento, es posible que la ventana asociada a un evento ya no exista en el momento en que se llama a la función de enlace. Los clientes deben comprobar que la ventana asociada a un evento todavía existe antes de realizar cualquier otra acción relacionada con el evento. Para asegurarse de que todavía existe una ventana, los clientes utilizan la función [**IsWindow**](/windows/desktop/api/winuser/nf-winuser-iswindow) de Microsoft Win32.
-   Si el archivo DLL en el que se define la función de enlace se vincula a otro archivo DLL, los desarrolladores de cliente deben asegurarse de que el sistema carga el otro archivo DLL. Si la vinculación implícita (mediante archivos. def e importaciones), el archivo DLL adicional debe estar en el directorio de Windows o en uno de los directorios del sistema, como Windows \\ System, Windows \\ system32 o Windows \\ SysWOW64. Si se vincula explícitamente (mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)), se debe especificar la ruta de acceso completa al directorio en el que reside el archivo dll adicional en la llamada a **LoadLibrary**.
-   Las funciones de enlace en contexto pueden producir un desbordamiento de pila cuando el archivo DLL que contiene la función de enlace se carga en una aplicación de 16 bits. Este problema se produce porque las aplicaciones de 16 bits usan un tamaño de pila fijo que no es lo suficientemente grande como para dar cabida a la cadena de llamadas de función del sistema que dan como resultado una llamada a la función de enlace.

## <a name="precautions-for-server-developers"></a>Precauciones para los desarrolladores de servidores

Los desarrolladores de servidores deben tener en cuenta que las aplicaciones cliente pueden registrar funciones de enlace en contexto. Cuando un servidor llama a [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent), debe estar preparado para controlar [**WM \_ GETOBJECT**](wm-getobject.md) y otros métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

## <a name="invalid-interface-pointers"></a>Punteros de interfaz no válidos

Cuando un cliente llama a [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) en una función de enlace en contexto, el puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que se devuelve apunta directamente al código en el espacio de direcciones del servidor. Si el cliente llama a una propiedad de interfaz mediante este puntero, la biblioteca del modelo de objetos componentes (COM) no está implicada en el cálculo de referencias (empaquetado y envío de parámetros de interfaz a través de los límites del proceso) o anulando la serialización (Desempaquetando los parámetros que se han enviado a través de los límites del proceso) y no detecta si se destruye un objeto

Si el cliente llama a una propiedad de interfaz para un objeto que se destruye, el puntero de interfaz no válido produce un error de protección general en el espacio de direcciones del servidor, a menos que el servidor detecte esta situación.

Para protegerse de los punteros de interfaz no válidos, los servidores [crean objetos proxy](creating-proxy-objects.md) que ajustan los objetos accesibles y supervisan el intervalo de vida de los objetos accesibles. Por ejemplo, cuando un cliente llama a una propiedad [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para obtener información sobre un objeto, el proxy comprueba si el objeto accesible sigue estando disponible y, en caso afirmativo, reenvía la solicitud del cliente al objeto accesible. Si se destruye el objeto accesible, el proxy devuelve un error al cliente.

 

 