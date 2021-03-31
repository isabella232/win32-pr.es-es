---
title: Ciclo de vida de la instancia de virtualización
description: Información general sobre el ciclo de vida de una instancia de virtualización de ProjFS.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: 567eff1f7b8acf330dba7c652e2e12b724072b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533238"
---
# <a name="virtualization-instance-lifecycle"></a>Ciclo de vida de la instancia de virtualización

La aplicación de proveedor mantiene una o más instancias de virtualización.  Cada instancia de virtualización pasa por cuatro fases en su ciclo de vida:

1. Creación
2. Inicio
3. Tiempo de ejecución
4. Apagar

Tenga en cuenta que después de apagar una instancia de virtualización, no es necesario que el proveedor vuelva a crearla para reutilizarla.  Simplemente puede iniciarla de nuevo.

> **Nota**: en esta sección se muestran ejemplos de API de ProjFS.  Cada ejemplo está pensado para ilustrar el uso básico de la API.  Para ver la documentación de las opciones que no se usan en estos ejemplos, consulte la referencia de la [API de ProjFS](/windows/desktop/api/_projfs).

## <a name="creating-a-virtualization-root"></a>Crear una raíz de virtualización

Para que un proveedor pueda iniciar la instancia de virtualización que va a proyectar los elementos en el sistema de archivos local, debe crear la raíz de virtualización.  La raíz de virtualización es el directorio en el que el proveedor proyecta un árbol de directorios y archivos.

Para crear una raíz de virtualización, el proveedor debe:

1. Cree un directorio para que sirva como raíz de virtualización.

    El proveedor crea un directorio para actuar como la raíz de virtualización mediante, por ejemplo, **[CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**:

    ```C++
    HRESULT hr;
    const wchar_t* rootName = LR"(C:\virtRoot)";
    if (!CreateDirectoryW(rootName, nullptr))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        wprintf(L"Failed to create virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

1. Cree un identificador de instancia de virtualización.

    Cada instancia de virtualización tiene un identificador único denominado _identificador de instancia de virtualización_.  El sistema utiliza este valor para identificar a qué instancia de virtualización está asociada su contenido.

    ```C++
    GUID instanceId;
    hr = CoCreateGuid(&instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to create instance ID (0x%08x)\n", hr);
        return;
    }
    ```

1. Marque el nuevo directorio como la raíz de virtualización.

    El proveedor llama a **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** para marcar el nuevo directorio como la raíz de virtualización y asignarlo a la instancia de virtualización.

    ```C++
    hr = PrjMarkDirectoryAsPlaceholder(rootName,
                                       nullptr,
                                       nullptr,
                                       &instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to mark virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

El proveedor solo necesita crear la raíz de virtualización una vez para cada instancia de virtualización.  Una vez creada una raíz, su instancia asociada puede iniciarse y detenerse repetidamente sin volver a crear la raíz.

## <a name="starting-a-virtualization-instance"></a>Iniciar una instancia de virtualización

Una vez creada la raíz de virtualización, el proveedor debe iniciar la instancia de virtualización.  Esto indica a ProjFS que el proveedor está listo para recibir devoluciones de llamada y proporcionar datos.

Para iniciar la instancia de virtualización, el proveedor debe:

1. Configure la tabla de devolución de llamada.

    ProjFS se comunica con el proveedor mediante la invocación de rutinas de devolución de llamada implementadas por el proveedor.  El proveedor rellena una [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) struct con punteros a sus rutinas de devolución de llamada.

    ```C++
    PRJ_CALLBACKS callbackTable;

    // Supply required callbacks.
    callbackTable.StartDirectoryEnumerationCallback = MyStartEnumCallback;
    callbackTable.EndDirectoryEnumerationCallback = MyEndEnumCallback;
    callbackTable.GetDirectoryEnumerationCallback = MyGetEnumCallback;
    callbackTable.GetPlaceholderInfoCallback = MyGetPlaceholderInfoCallback;
    callbackTable.GetFileDataCallback = MyGetFileDataCallback;

    // The rest of the callbacks are optional.
    callbackTable.QueryFileNameCallback = nullptr;
    callbackTable.NotificationCallback = nullptr;
    callbackTable.CancelCommandCallback = nullptr;
    ```

1. Inicie la instancia de.

    El proveedor llama a **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** para iniciar la instancia de virtualización.

    ```C++
    PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT instanceHandle;
    hr = PrjStartVirtualizing(rootName,
                              &callbackTable,
                              nullptr,
                              nullptr,
                              &instanceHandle);
    if (FAILED(hr))
    {
        wprintf(L"Failed to start the virtualization instance (0x%08x)\n", hr);
        return;
    }
    ```
    El parámetro _instanceHandle_ de **PrjStartVirtualizing** devuelve un identificador a la instancia de virtualización.  El proveedor usa este controlador al llamar a otras API de ProjFS.

## <a name="virtualization-instance-runtime"></a>Tiempo de ejecución de instancia de virtualización

Una vez que se devuelve la llamada a **PrjStartVirtualizing** , ProjFS invocará las rutinas de devolución de llamada del proveedor en respuesta a las operaciones del sistema de archivos en la instancia de virtualización.  Para obtener información sobre cómo el proveedor puede controlar varias operaciones del sistema de archivos, consulte las secciones siguientes:

* [Enumeración de archivos y directorios](enumerating-files-and-directories.md)
* [Aprovisionamiento de datos de archivo](providing-file-data.md)
* [Notificaciones de operación del sistema de archivos](file-system-operation-notifications.md)
* [Control de cambios de vista](handling-view-changes.md)

## <a name="shutting-down-a-virtualization-instance"></a>Cerrar una instancia de virtualización

Para indicar a ProjFS que el proveedor desea dejar de recibir devoluciones de llamada y proporcionar datos, el proveedor debe detener la instancia de virtualización.  Para ello, el proveedor llama a **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**, pasándole el identificador a la instancia de virtualización que recibió de la llamada a **PrjStartVirtualizing**.

```C++
PrjStopVirtualizing(instanceHandle);
```

Tenga en cuenta que hasta que se devuelve esta llamada, ProjFS puede continuar invocando las rutinas de devolución de llamada del proveedor.