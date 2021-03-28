---
description: Determina si se permitirá que el shell mueva, copie, elimine o cambie el nombre de una carpeta en la raíz de sincronización de un proveedor de nube.
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
ms.openlocfilehash: c7df9296f2261e3907702067ca36265095102f34
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104997985"
---
# <a name="istorageprovidercopyhookcopycallback-method"></a>IStorageProviderCopyHook:: CopyCallback (método)

Determina si se permitirá que el shell mueva, copie, elimine o cambie el nombre de una carpeta en la raíz de sincronización de un proveedor de nube.

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

*hWnd* \[ de\]
</dt> <dd>

Identificador de la ventana que el controlador de enlace de copia debe usar como elemento primario para los elementos de la interfaz de usuario que el controlador puede necesitar Mostrar. Si se especifica **FOF_SILENT** en la *operación*, el método debe omitir este parámetro.

</dd> </dl>

<dl> <dt>

*operación* \[ de de\]
</dt> <dd>

Operación que se va a realizar. Este parámetro puede ser uno de los valores enumerados en el miembro **wFunc** de la estructura [SHFILEOPSTRUCT](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa) .

</dd> </dl>

<dl> <dt>

*marcas* \[ de de\]
</dt> <dd>

Marcas que controlan la operación. Este parámetro puede ser uno o varios de los valores enumerados en el miembro *fFlags* de la estructura [SHFILEOPSTRUCT](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) .

En el caso de los enlaces de copia de impresora, este valor es uno de los siguientes valores definidos en ShellAPI. h.

| Value       | Descripción |
|-------------|------------|
|  **PO_DELETE**      | Se está eliminando una impresora. El parámetro *srcFile* apunta a la ruta de acceso completa a la impresora especificada.           |
|  **PO_RENAME**       | Se va a cambiar el nombre de una impresora. El parámetro *srcFile* apunta al nuevo nombre de la impresora. El parámetro *destFile* apunta al nombre anterior.           |
| **PO_PORTCHANGE**    | No se admite. No debe usarse.          |
| **PO_REN_PORT**    | No se admite. No debe usarse.           |

</dd> </dl>

<dl> <dt>

*srcFile* \[ de\]
</dt> <dd>

Puntero a una cadena que contiene el nombre de la carpeta de origen.

</dd> </dl>

*srcAttribs* \[ de\]
</dt> <dd>

Atributos de la carpeta de origen. Este parámetro puede ser una combinación de cualquiera de las marcas de atributo de archivo (FILE_ATTRIBUTE_ *) definidas en los archivos de encabezado. Vea [constantes de atributo de archivo](../fileio/file-attribute-constants.md).

</dd> </dl>

*destFile* \[ de\]
</dt> <dd>

Puntero a una cadena que contiene el nombre de la carpeta de destino.

</dd> </dl>

*destAttribs* \[ de\]
</dt> <dd>

Atributos de la carpeta de destino. Este parámetro puede ser una combinación de cualquiera de las marcas de atributo de archivo (FILE_ATTRIBUTE_ *) definidas en los archivos de encabezado. Vea [constantes de atributo de archivo](../fileio/file-attribute-constants.md).

</dd> </dl>

*resultado* \[ de enuncia\]
</dt> <dd>

Valor entero que indica si el shell debe realizar la operación. Uno de los siguientes:

| Valor       | Descripción |
|-------------|------------|
| **IDYES**       | Permite la operación.           |
| **IDNO**        | Evita la operación en esta carpeta pero continúa con cualquier otra operación que se haya aprobado (por ejemplo, una operación de copia por lotes).           |
| **IDCANCEL**    | Evita la operación actual y cancela las operaciones pendientes.           |


</dd> </dl>


## <a name="return-value"></a>Valor devuelto

Devuelve **S_OK** si se realiza correctamente, o un código de error en caso contrario.

## <a name="remarks"></a>Observaciones

El shell llama al controlador de enlace de copia del proveedor de la nube para cada carpeta en la raíz de sincronización registrada. Para registrar un controlador de enlace de copia para las carpetas en la nube, establezca el valor de **CopyHook** en la clave de **/software/Microsoft/Windows/CurrentVersion/Explorer/syncrootmanager/{syncrootid} HKEY_LOCAL_MACHINE** en el CLSID del objeto de enlace de copia.

Cuando se llama al método **CopyCallback** , el shell inicializa la interfaz [IStorageProviderCopyHook](nn-shobjidl-istorageprovidercopyhook.md) directamente sin usar una interfaz [IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) en primer lugar.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Compilación 19624 de Windows 10 Insider Preview                                |
| Encabezado                   | shobjidl. h   |

## <a name="see-also"></a>Vea también

[Compilar un motor de sincronización en la nube que admita archivos de marcadores de posición](../cfapi/build-a-cloud-file-sync-engine.md)