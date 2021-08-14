---
description: Determina si shell podrá mover, copiar, eliminar o cambiar el nombre de una carpeta en la raíz de sincronización de un proveedor de nube.
title: IStorageProviderCopyHook::CopyCallback
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook::CopyCallback
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: 26fe9079e7fdf53809f8c0763fa38f271536f1339d16647936fb141f8d213be5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677983"
---
# <a name="istorageprovidercopyhookcopycallback-method"></a>IStorageProviderCopyHook::CopyCallback (Método)

Determina si shell podrá mover, copiar, eliminar o cambiar el nombre de una carpeta en la raíz de sincronización de un proveedor de nube.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT CopyCallback( 
    HWND hwnd,
    UINT operation,
    UINT flags,
    LPCWSTR srcFile,
    DWORD srcAttribs,
    LPCWSTR destFile,
    DWORD destAttribs,
    UINT* result
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwnd* \[ En\]
</dt> <dd>

Identificador de la ventana que el controlador de enlace de copia debe usar como elemento primario para cualquier elemento de la interfaz de usuario que el controlador deba mostrar. Si **FOF_SILENT** especifica en la *operación*, el método debe omitir este parámetro.

</dd> </dl>

<dl> <dt>

*operación* \[ En\]
</dt> <dd>

Operación que se va a realizar. Este parámetro puede ser uno de los valores enumerados en el **miembro wFunc** de la [estructura SHFILEOPSTRUCT.](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa)

</dd> </dl>

<dl> <dt>

*flags* \[ En\]
</dt> <dd>

Marcas que controlan la operación. Este parámetro puede ser uno o varios de los valores enumerados en el *miembro fFlags* de la [estructura SHFILEOPSTRUCT.](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa)

Para los enlaces de copia de impresora, este valor es uno de los siguientes valores definidos en shellapi.h.

| Valor       | Descripción |
|-------------|------------|
|  **PO_DELETE**      | Se está eliminando una impresora. El *parámetro srcFile* apunta a la ruta de acceso completa a la impresora especificada.           |
|  **PO_RENAME**       | Se va a cambiar el nombre de una impresora. El *parámetro srcFile* apunta al nuevo nombre de la impresora. El *parámetro destFile* apunta al nombre antiguo.           |
| **PO_PORTCHANGE**    | No compatible. No debe usarse.          |
| **PO_REN_PORT**    | No compatible. No debe usarse.           |

</dd> </dl>

<dl> <dt>

*srcFile* \[ En\]
</dt> <dd>

Puntero a una cadena que contiene el nombre de la carpeta de origen.

</dd> </dl>

*srcAttribs* \[ En\]
</dt> <dd>

Atributos de la carpeta de origen. Este parámetro puede ser una combinación de cualquiera de las marcas de atributo de archivo (FILE_ATTRIBUTE_*) definidas en los archivos de encabezado. Vea File Attribute Constants (Constantes [de atributo de archivo).](../fileio/file-attribute-constants.md)

</dd> </dl>

*destFile* \[ En\]
</dt> <dd>

Puntero a una cadena que contiene el nombre de la carpeta de destino.

</dd> </dl>

*destAttribs* \[ En\]
</dt> <dd>

Atributos de la carpeta de destino. Este parámetro puede ser una combinación de cualquiera de las marcas de atributo de archivo (FILE_ATTRIBUTE_*) definidas en los archivos de encabezado. Vea File Attribute Constants (Constantes [de atributo de archivo).](../fileio/file-attribute-constants.md)

</dd> </dl>

*resultado* \[ out\]
</dt> <dd>

Valor entero que indica si el Shell debe realizar la operación. Uno de los siguientes:

| Valor       | Descripción |
|-------------|------------|
| **IDYES**       | Permite la operación.           |
| **IDNO**        | Impide la operación en esta carpeta, pero continúa con cualquier otra operación que se haya aprobado (por ejemplo, una operación de copia por lotes).           |
| **IDCANCEL**    | Impide la operación actual y cancela las operaciones pendientes.           |


</dd> </dl>


## <a name="return-value"></a>Valor devuelto

Devuelve **S_OK** si se realiza correctamente o un código de error de lo contrario.

## <a name="remarks"></a>Comentarios

Shell llama al controlador de enlace de copia del proveedor de nube para cada carpeta de la raíz de sincronización registrada. Para registrar un controlador de enlace de copia para carpetas en la nube, establezca el valor **de CopyHook** en la clave **HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Explorer/SyncRootManager/{SyncRootId}** en el CLSID del objeto de enlace de copia.

Cuando se **llama al método CopyCallback,** el shell inicializa la interfaz [IStorageProviderCopyHook](nn-shobjidl-istorageprovidercopyhook.md) directamente sin usar primero una [interfaz IShellExtInit.](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 10 Insider Preview Build 19624                                |
| Header                   | shobjidl.h   |

## <a name="see-also"></a>Consulte también

[Compilación de un motor de Sincronización en la nube que admita archivos de marcador de posición](../cfapi/build-a-cloud-file-sync-engine.md)