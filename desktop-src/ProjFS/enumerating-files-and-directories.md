---
title: Enumeración de archivos y directorios
description: Describe cómo un proveedor ProjFS participa en la enumeración de directorios.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/25/2018
ms.topic: article
ms.openlocfilehash: 606b379e206cdbc64726e0ea97aed34e00f5253ecbffb7f8b7d42469b0cbb5fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792818"
---
# <a name="enumerating-files-and-directories"></a>Enumeración de archivos y directorios

Cuando un proveedor crea por primera vez una raíz de virtualización, está vacío en el sistema local.  Es decir, ninguno de los elementos del almacén de datos de respaldo todavía se ha almacenado en caché en el disco.  A medida que se abre cada elemento, se almacena en caché, pero hasta que se abre un elemento solo existe en el almacén de datos de respaldo.

Puesto que los elementos sin abrir no tienen presencia local, la enumeración de directorios normales no revelaría su existencia al usuario.  Por lo tanto, el proveedor debe participar en la enumeración de directorios devolviendo información a ProjFS sobre los elementos de su almacén de datos de respaldo.  ProjFS combina la información del proveedor con lo que hay en el sistema de archivos local para presentar al usuario una lista unificada del contenido de un directorio.

## <a name="directory-enumeration-callbacks"></a>Devoluciones de llamada de enumeración de directorios

Para participar en la enumeración de directorios, el proveedor debe implementar PRJ_START_DIRECTORY_ENUMERATION_CB **[,](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** y **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** devoluciones de llamada.  Cuando se enumera un directorio bajo la raíz de virtualización del proveedor, ProjFS realiza las siguientes acciones:

1. ProjFS llama a la devolución de llamada **PRJ_START_DIRECTORY_ENUMERATION_CB** del proveedor para iniciar una sesión de enumeración.

    Como parte del procesamiento de esta devolución de llamada, el proveedor debe prepararse para realizar la enumeración.  Por ejemplo, debe asignar cualquier memoria que necesite para realizar un seguimiento del progreso de la enumeración en su almacén de datos de respaldo.

    ProjFS identifica el directorio que se enumera en el miembro **FilePathName** del parámetro _callbackData_ de la devolución de llamada.  Se especifica como una ruta de acceso relativa a la raíz de virtualización.  Por ejemplo, si la raíz de virtualización se encuentra en y el directorio que se `C:\virtRoot` enumera es , el miembro `C:\virtRoot\dir1\dir2` **FilePathName** contendrá `dir1\dir2` .  El proveedor se preparará para enumerar esa ruta de acceso en su almacén de datos de respaldo.  En función de las funcionalidades del almacén de respaldo de un proveedor, puede tener sentido realizar la enumeración del almacén de respaldo en la **devolución** PRJ_START_DIRECTORY_ENUMERATION_CB de llamada.

    Dado que pueden producirse varias enumeraciones en paralelo en el mismo directorio, cada devolución de llamada de enumeración tiene un argumento _enumerationId_ para permitir que el proveedor asocie las invocaciones de devolución de llamada a una sola sesión de enumeración.

    Si el proveedor devuelve S_OK de la devolución de llamada **de PRJ_START_DIRECTORY_ENUMERATION_CB,** debe mantener cualquier información de sesión de enumeración que tenga hasta que ProjFS invoque la devolución de llamada **PRJ_END_DIRECTORY_ENUMERATION_CB** con el mismo valor para _enumerationId_.  Si el proveedor devuelve un error de **PRJ_START_DIRECTORY_ENUMERATION_CB**,  ProjFS no invocará la devolución de llamada PRJ_END_DIRECTORY_ENUMERATION_CB para _ese enumerationId_.

1. ProjFS llama a la devolución de llamada **PRJ_GET_DIRECTORY_ENUMERATION_CB** del proveedor una o varias veces para obtener el contenido del directorio del proveedor.

    En respuesta a esta devolución de llamada, el proveedor devuelve una lista ordenada de elementos de su almacén de datos de respaldo.

    La devolución de llamada puede proporcionar una expresión de búsqueda en su _parámetro searchExpression_ que el proveedor usa para ámbito de los resultados de la enumeración.  Si _searchExpression_ es NULL, el proveedor devuelve todas las entradas del directorio que se enumera.  Si no es NULL, el proveedor puede usar **[PrjDoesNameContainWildCards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** para determinar si hay caracteres comodín en la expresión.  Si lo hay, el proveedor usa **[PrjFileNameMatch para](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** determinar si una entrada del directorio coincide con la expresión de búsqueda.

    El proveedor debe capturar el valor de _searchExpression_ en la primera invocación de esta devolución de llamada.  Usa el valor capturado en cualquier invocación posterior de la devolución de llamada en la misma sesión de enumeración, a menos que PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN se establezca en el campo **Flags** del parámetro _callbackData_ de la devolución de llamada.  En ese caso, debe volver a capturar el valor de _searchExpression_.

    Si no hay entradas que coincidan en su almacén de respaldo, el proveedor simplemente devuelve S_OK de la devolución de llamada.  De lo contrario, el proveedor da formato a cada entrada correspondiente de su almacén de respaldo en una estructura PRJ_FILE_BASIC_INFO y, **[a](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** continuación, usa **[PrjFillDirEntryBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** para rellenar el búfer proporcionado por el parámetro _dirEntryBufferHandle_ de la devolución de llamada.  El proveedor sigue agregando entradas hasta que las ha agregado todas o hasta **que PrjFillDirEntryBuffer** devuelve HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER).  Después, el proveedor devuelve S_OK de la devolución de llamada.  Tenga en cuenta que el proveedor debe agregar las entradas al búfer _dirEntryBufferHandle_ en el criterio de ordenación correcto.  El proveedor debe usar **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** para determinar el criterio de ordenación correcto.

    > El proveedor debe proporcionar un valor para el **miembro IsDirectory** de **PRJ_FILE_BASIC_INFO**.  Si **IsDirectory** es FALSE, el proveedor también debe proporcionar un valor para el **miembro FileSize.**
    >
    > Si el proveedor no proporciona valores para los miembros **CreationTime**, **LastAccessTime**, **LastWriteTime** y **ChangeTime,** ProjFS usará la hora actual del sistema.
    >
    > ProjFS usará cualquier marca FILE_ATTRIBUTE los conjuntos de proveedores en el **miembro FileAttributes,** excepto para FILE_ATTRIBUTE_DIRECTORY; establecerá el valor correcto para FILE_ATTRIBUTE_DIRECTORY en el **miembro FileAttributes** según el valor proporcionado del **miembro IsDirectory.**

    Si **PrjFillDirEntryBuffer** devuelve HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) antes de que el proveedor se queda sin entradas para agregarle, el proveedor debe realizar un seguimiento de la entrada que estaba intentando agregar cuando recibió el error.  La próxima vez que ProjFS llame PRJ_GET_DIRECTORY_ENUMERATION_CB la devolución de llamada de **PRJ_GET_DIRECTORY_ENUMERATION_CB** para la misma sesión de enumeración, el proveedor debe reanudar la adición de entradas al búfer _dirEntryBufferHandle_ con la entrada que estaba intentando agregar.

    > Si el almacén de respaldo admite vínculos simbólicos, el proveedor debe usar **[PrjFillDirEntryBuffer2 para](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** rellenar el búfer proporcionado por el parámetro _dirEntryBufferHandle_ de la devolución de llamada.  **PrjFillDirEntryBuffer2** admite una entrada de búfer adicional que permite al proveedor especificar que la entrada de enumeración es un vínculo simbólico y cuál es su destino.  De lo contrario, se comporta como se ha descrito anteriormente para **PrjFillDirEntryBuffer.**  En el ejemplo siguiente se **usa PrjFillDirEntryBuffer2 para** ilustrar la compatibilidad con vínculos simbólicos.
    >
    > Tenga en **cuenta que PrjFillDirEntryBuffer2** se admite a partir Windows 10, versión 2004.  Un proveedor debe sondear la existencia de **PrjFillDirEntryBuffer2,** por ejemplo, mediante **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.

    ```C++
    typedef struct MY_ENUM_ENTRY MY_ENUM_ENTRY;

    typedef struct MY_ENUM_ENTRY {
        MY_ENUM_ENTRY* Next;
        PWSTR Name;
        BOOLEAN IsDirectory;
        INT64 FileSize;
        BOOLEAN IsSymlink;
        PWSTR SymlinkTarget;
    } MY_ENUM_ENTRY;

    typedef struct MY_ENUM_SESSION {
        GUID EnumerationId;
        PWSTR SearchExpression;
        USHORT SearchExpressionMaxLen;
        BOOLEAN SearchExpressionCaptured;
        MY_ENUM_ENTRY* EnumHead;
        MY_ENUM_ENTRY* LastEnumEntry;
        BOOLEAN EnumCompleted;
    } MY_ENUM_SESSION;

    HRESULT
    MyGetEnumCallback(
        _In_ const PRJ_CALLBACK_DATA* callbackData,
        _In_ const GUID* enumerationId,
        _In_opt_z_ PCWSTR searchExpression,
        _In_ PRJ_DIR_ENTRY_BUFFER_HANDLE dirEntryBufferHandle
        )
    {
        // MyGetEnumSession is a routine the provider might implement to find
        // information about the enumeration session that it first stored
        // when processing its PRJ_START_DIRECTORY_ENUMERATION_CB callback.
        //
        // In this example the PRJ_START_DIRECTORY_ENUMERATION_CB callback has
        // already retrieved a list of the items in the backing store located at
        // callbackData->FilePathName, sorted them using PrjFileNameCompare()
        // to determine collation order, and stored the list in session->EnumHead.
        MY_ENUM_SESSION* session = NULL;
        session = MyGetEnumSession(enumerationId);

        if (session == NULL)
        {
            return HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER);
        }

        if (!session->SearchExpressionCaptured ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            if (searchExpression != NULL)
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              searchExpression,
                              wcslen(searchExpression)))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            else
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              "*",
                              1))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            session->SearchExpressionCaptured = TRUE;
        }

        MY_ENUM_ENTRY* enumHead = NULL;

        // We have to start the enumeration from the beginning if we aren't
        // continuing an existing session or if the caller is requesting a restart.
        if (((session->LastEnumEntry == NULL) &&
             !session->EnumCompleted) ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            // Ensure that if the caller is requesting a restart we reset our
            // bookmark of how far we got in the enumeration.
            session->LastEnumEntry = NULL;

            // In case we're restarting ensure we don't think we're done.
            session->EnumCompleted = FALSE;

            // We need to start considering items from the beginning of the list
            // retrieved from the backing store.
            enumHead = session->EnumHead;
        }
        else
        {
            // We are resuming an existing enumeration session.  Note that
            // session->LastEnumEntry may be NULL.  That is okay; it means
            // we got all the entries the last time this callback was invoked.
            // Returning S_OK without adding any new entries to the
            // dirEntryBufferHandle buffer signals ProjFS that the enumeration
            // has returned everything it can.
            enumHead = session->LastEnumEntry;
        }

        if (enumHead == NULL)
        {
            // There are no items to return.  Remember that we've returned everything
            // we can.
            session->EnumCompleted = TRUE;
        }
        else
        {
            MY_ENUM_ENTRY* thisEntry = enumHead;
            while (thisEntry != NULL)
            {
                // We'll insert the entry into the return buffer if it matches
                // the search expression captured for this enumeration session.
                if (PrjFileNameMatch(thisEntry->Name, session->SearchExpression))
                {
                    PRJ_FILE_BASIC_INFO fileBasicInfo = {};
                    fileBasicInfo.IsDirectory = thisEntry->IsDirectory;
                    fileBasicInfo.FileSize = thisEntry->FileSize;

                    // If our backing store says this is really a symbolic link,
                    // set up to tell ProjFS that it is a symlink and what its
                    // target is.
                    PRJ_EXTENDED_INFO extraInfo = {};
                    if (thisEntry->IsSymlink)
                    {
                        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
                        extraInfo.Symlink.TargetName = thisEntry->SymlinkTarget;
                    }

                    // Format the entry for return to ProjFS.
                    HRESULT fillResult = PrjFillDirEntryBuffer2(dirEntryBufferHandle,
                                                                thisEntry->Name,
                                                                &fileBasicInfo,
                                                                thisEntry->IsSymlink ? &extraInfo : NULL);

                    if (fillResult == HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER))
                    {
                        // We couldn't add this entry to the buffer; remember where we left
                        // off for the next time we're called for this enumeration session.
                        session->LastEnumEntry = thisEntry;
                        return S_OK;
                    }
                }

                thisEntry = thisEntry->Next;
            }

            // We reached the end of the list of entries; remember that we've returned
            // everything we can.
            session->EnumCompleted = TRUE;
        }

        return S_OK;
    }
    ```

1. ProjFS llama a la devolución de llamada **PRJ_END_DIRECTORY_ENUMERATION_CB** del proveedor para finalizar la sesión de enumeración.

    El proveedor debe realizar cualquier limpieza que deba realizar para finalizar la sesión de enumeración, como desasignar la memoria asignada como parte del procesamiento de **PRJ_START_DIRECTORY_ENUMERATION_CB**.
