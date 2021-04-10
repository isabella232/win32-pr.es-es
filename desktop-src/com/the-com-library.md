---
title: Biblioteca COM
description: Biblioteca COM
ms.assetid: 51d4db4a-ad88-4627-8140-2f7906945752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a285a89ca659907c37f92b7d00f3e3e04d0acf51
ms.sourcegitcommit: 307b14e9847ced354a52a1ac12d7f659722d99bb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/06/2020
ms.locfileid: "103995007"
---
# <a name="the-com-library"></a>Biblioteca COM

Cualquier proceso que use COM debe inicializar y anular la inicialización de la biblioteca COM. Además de ser una especificación, COM también implementa algunos servicios importantes en esta biblioteca. La biblioteca COM, que se proporciona como un conjunto de archivos dll y exe (principalmente Ole32.dll y Rpcss.exe) en Microsoft Windows, incluye lo siguiente:

-   Un pequeño número de funciones fundamentales que facilitan la creación de aplicaciones COM, tanto de cliente como de servidor. En el caso de los clientes, COM proporciona funciones básicas para crear objetos. En el caso de los servidores, COM proporciona los medios para exponer sus objetos.

-   Los servicios de ubicación de implementación a través de los cuales COM determinan, desde un identificador de clase único (CLSID), que el servidor implementa esa clase y donde se encuentra el servidor. Este servicio incluye compatibilidad con un nivel de direccionamiento indirecto, normalmente un registro del sistema, entre la identidad de una clase de objeto y el empaquetado de la implementación para que los clientes sean independientes del empaquetado, lo que puede cambiar en el futuro.

-   Llamadas a procedimiento remoto transparentes cuando un objeto se está ejecutando en un servidor local o remoto.

-   Mecanismo estándar para permitir que una aplicación controle el modo en que se asigna la memoria dentro de su proceso, especialmente la memoria que debe pasarse entre los objetos cooperativos para que se pueda liberar correctamente.

Para usar servicios COM básicos, todos los subprocesos COM de ejecución en clientes y servidores fuera de proceso deben llamar a la función [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) antes de llamar a cualquier otra función com, excepto las llamadas de asignación de memoria. **CoInitializeEx** reemplaza la otra función, agregando un parámetro que le permite especificar el modelo de subprocesos del subproceso, ya sea de apartamento o de subproceso libre. Una llamada a **CoInitialize** simplemente establece el modelo de subprocesos en Apartamento-threaded.

Las aplicaciones de documentos compuestos OLE llaman a la función [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize) , que llama a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) y también requiere una inicialización para los documentos compuestos. Por lo tanto, los subprocesos que llaman a **OleInitialize** no pueden ser de subproceso libre. Para obtener información sobre los subprocesos en clientes y servidores, consulte [procesos, subprocesos y apartamentos](processes--threads--and-apartments.md).

Los servidores en proceso no llaman a las funciones de inicialización porque se cargan en un proceso que ya lo ha hecho. Como resultado, los servidores en proceso deben establecer su modelo de subprocesos en el registro con la clave [InProcServer32](inprocserver32.md) . Para obtener información detallada sobre los problemas de subprocesos en los servidores de proceso, vea [problemas de subprocesos de servidor en proceso](in-process-server-threading-issues.md).

También es importante anular la inicialización de la biblioteca. Para cada llamada a [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), debe haber una llamada correspondiente a [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize). Para cada llamada a [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize), debe haber una llamada correspondiente a [**OleUninitialize**](/windows/desktop/api/Ole2/nf-ole2-oleuninitialize).

Los servidores en proceso pueden suponer que el proceso en el que se cargan ya ha realizado estos pasos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[The Component Object Model](the-component-object-model.md) [Modelo de objetos componentes (COM)]
</dt> </dl>

 

 




