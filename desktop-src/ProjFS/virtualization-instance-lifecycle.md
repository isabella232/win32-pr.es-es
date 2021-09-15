---
title: Ciclo de vida de la instancia de virtualización
description: Información general sobre el ciclo de vida de una instancia de virtualización de ProjFS.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: 567eff1f7b8acf330dba7c652e2e12b724072b9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473634"
---
# <a name="virtualization-instance-lifecycle"></a>Ciclo de vida de la instancia de virtualización

La aplicación del proveedor mantiene una o varias instancias de virtualización.  Cada instancia de virtualización pasa por cuatro fases de su ciclo de vida:

1. Creación
2. Inicio
3. Tiempo de ejecución
4. Apagar

Tenga en cuenta que después de apagar una instancia de virtualización, el proveedor no necesita volver a crearla para reutilizarla.  Simplemente puede iniciarlo de nuevo.

> **Nota:** En esta sección se muestran ejemplos de API de ProjFS.  Cada ejemplo está pensado para ilustrar el uso básico de la API.  Para obtener documentación sobre las opciones que no se usan en estos ejemplos, consulte la referencia de [api de ProjFS](/windows/desktop/api/_projfs).

## <a name="creating-a-virtualization-root"></a>Creación de una raíz de virtualización

Para que un proveedor pueda iniciar la instancia de virtualización que proyectará elementos en el sistema de archivos local, debe crear la raíz de virtualización.  La raíz de virtualización es el directorio en el que el proveedor proyecta un árbol de directorios y archivos.

Para crear una raíz de virtualización, el proveedor debe:

1. Cree un directorio que sirva como raíz de virtualización.

    El proveedor crea un directorio que sirve como raíz de virtualización mediante, por **[ejemplo, CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**:

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

    Cada instancia de virtualización tiene un identificador único denominado identificador _de instancia de virtualización._  El sistema usa este valor para identificar a qué instancia de virtualización está asociado su contenido.

    ```C++
    GUID instanceId;
    hr = CoCreateGuid(&instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to create instance ID (0x%08x)\n", hr);
        return;
    }
    ```

1. Marque el nuevo directorio como raíz de virtualización.

    El proveedor llama **[a PrjMarkDirectoryAsPlaceholder para](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** marcar el nuevo directorio como raíz de virtualización y asignarlo a la instancia de virtualización.

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

El proveedor solo necesita crear la raíz de virtualización una vez para cada instancia de virtualización.  Una vez creada una raíz, su instancia asociada se puede iniciar y detener repetidamente sin volver a crear la raíz.

## <a name="starting-a-virtualization-instance"></a>Inicio de una instancia de virtualización

Una vez creada la raíz de virtualización, el proveedor debe iniciar la instancia de virtualización.  Esto indica a ProjFS que el proveedor está listo para recibir devoluciones de llamada y proporcionar datos.

Para iniciar la instancia de virtualización, el proveedor debe:

1. Configure la tabla de devolución de llamada.

    ProjFS se comunica con el proveedor invocando rutinas de devolución de llamada implementadas por el proveedor.  El proveedor rellena un [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) struct con punteros a sus rutinas de devolución de llamada.

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

1. Inicie la instancia de .

    El proveedor llama **[a PrjStartVirtualizing para](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** iniciar la instancia de virtualización.

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
    **El parámetro instanceHandle de PrjStartVirtualizing** devuelve un identificador a la instancia de virtualización.   El proveedor usa este identificador al llamar a otras API de ProjFS.

## <a name="virtualization-instance-runtime"></a>Entorno de ejecución de instancia de virtualización

Una vez que se devuelve la llamada a **PrjStartVirtualizing,** ProjFS invocará las rutinas de devolución de llamada del proveedor en respuesta a las operaciones del sistema de archivos en la instancia de virtualización.  Para obtener información sobre cómo el proveedor puede controlar varias operaciones del sistema de archivos, consulte las secciones siguientes:

* [Enumeración de archivos y directorios](enumerating-files-and-directories.md)
* [Aprovisionamiento de datos de archivo](providing-file-data.md)
* [Notificaciones de operación del sistema de archivos](file-system-operation-notifications.md)
* [Control de cambios en la vista](handling-view-changes.md)

## <a name="shutting-down-a-virtualization-instance"></a>Apagar una instancia de virtualización

Para indicar a ProjFS que el proveedor quiere dejar de recibir devoluciones de llamada y proporcionar datos, el proveedor debe detener la instancia de virtualización.  Para ello, el proveedor llama a **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**, pasando el identificador a la instancia de virtualización que recibió de la llamada a **PrjStartVirtualizing**.

```C++
PrjStopVirtualizing(instanceHandle);
```

Tenga en cuenta que hasta que se devuelva esta llamada, ProjFS puede seguir invocando las rutinas de devolución de llamada del proveedor.