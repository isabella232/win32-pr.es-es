---
title: La biblioteca COM
description: La biblioteca COM
ms.assetid: 51d4db4a-ad88-4627-8140-2f7906945752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a285a89ca659907c37f92b7d00f3e3e04d0acf51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253142"
---
# <a name="the-com-library"></a>La biblioteca COM

Cualquier proceso que use COM debe inicializar y cancelar la inicialización de la biblioteca COM. Además de ser una especificación, COM también implementa algunos servicios importantes en esta biblioteca. Se proporciona como un conjunto de archivos DLL y EXE (principalmente Ole32.dll y Rpcss.exe) en Microsoft Windows, la biblioteca COM incluye lo siguiente:

-   Un pequeño número de funciones fundamentales que facilitan la creación de aplicaciones COM, tanto de cliente como de servidor. Para los clientes, COM proporciona funciones básicas para crear objetos. Para los servidores, COM proporciona los medios para exponer sus objetos.

-   Servicios de localizador de implementación a través de los cuales COM determina, a partir de un identificador de clase único (CLSID), qué servidor implementa esa clase y dónde se encuentra ese servidor. Este servicio incluye compatibilidad con un nivel de direccionamiento indirecto, normalmente un registro del sistema, entre la identidad de una clase de objeto y el empaquetado de la implementación para que los clientes sean independientes del empaquetado, lo que puede cambiar en el futuro.

-   El procedimiento remoto transparente llama a cuando un objeto se ejecuta en un servidor local o remoto.

-   Mecanismo estándar para permitir que una aplicación controle cómo se asigna la memoria dentro de su proceso, especialmente la memoria que debe pasarse entre objetos de cooperación para que se pueda liberar correctamente.

Para usar servicios COM básicos, todos los subprocesos COM de ejecución en clientes y servidores fuera de proceso deben llamar a la función [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) antes de llamar a cualquier otra función COM, excepto las llamadas de asignación de memoria. **CoInitializeEx** reemplaza la otra función, agregando un parámetro que permite especificar el modelo de subprocesos del subproceso: apartment-threaded o free-threaded. Una llamada a **CoInitialize** simplemente establece el modelo de subprocesos en apartment-threaded.

Las aplicaciones de documentos compuestos OLE llaman a la función [**OleInitialize,**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize) que llama a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) y también realiza alguna inicialización necesaria para los documentos compuestos. Por lo tanto, los subprocesos **que llaman a OleInitialize** no pueden ser de subproceso libre. Para obtener información sobre el subprocesamiento en clientes y servidores, vea [Procesos, subprocesos y departamentos.](processes--threads--and-apartments.md)

Los servidores en proceso no llaman a las funciones de inicialización porque se cargan en un proceso que ya lo ha hecho. Como resultado, los servidores en proceso deben establecer su modelo de subprocesos en el Registro bajo la [clave InprocServer32.](inprocserver32.md) Para obtener información detallada sobre los problemas de subprocesos en servidores en proceso, vea [In-Process Server Threading Issues](in-process-server-threading-issues.md).

También es importante desinicializar la biblioteca. Para cada llamada a [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), debe haber una llamada correspondiente a [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize). Para cada llamada a [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize), debe haber una llamada correspondiente a [**OleUninitialize**](/windows/desktop/api/Ole2/nf-ole2-oleuninitialize).

Los servidores en proceso pueden suponer que el proceso en el que se cargan ya ha realizado estos pasos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[The Component Object Model](the-component-object-model.md) [Modelo de objetos componentes (COM)]
</dt> </dl>

 

 




