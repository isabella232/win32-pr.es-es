---
description: Guarda una clave privada y su clave pública correspondiente en un archivo especificado.
ms.assetid: 491a128a-b4aa-4cca-a835-d0e8d7df6720
title: Función PvkPrivateKeySave
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeySave
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 3a2eed4b907f7c22414634a4b1ef49df6ca780181109a7396de2f8aa1776b7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901214"
---
# <a name="pvkprivatekeysave-function"></a>Función PvkPrivateKeySave

> [!IMPORTANT]
> Esta API está en desuso. Microsoft puede quitar esta API en futuras versiones.

 

La **función PvkPrivateKeySave** guarda una clave privada [*y*](../secgloss/p-gly.md) su clave [*pública correspondiente*](../secgloss/p-gly.md) en un archivo especificado.

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI PvkPrivateKeySave(
  _In_ HCRYPTPROV hCryptProv,
  _In_ HANDLE     hFile,
  _In_ DWORD      dwKeySpec,
  _In_ HWND       hwndOwner,
  _In_ LPCWSTR    pwszKeyName,
  _In_ DWORD      dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hCryptProv* \[ En\]
</dt> <dd>

Identificador de un proveedor [*de servicios criptográficos*](../secgloss/c-gly.md) (CSP).

</dd> <dt>

*hFile* \[ En\]
</dt> <dd>

Identificador de un archivo creado con el permiso inicial de lectura/escritura y el permiso de solo lectura subsiguiente.

</dd> <dt>

*dwKeySpec* \[ En\]
</dt> <dd>

Entero largo para el tipo de clave. Los valores posibles **incluyen AT \_ KEYEXCHANGE** o **AT \_ SIGNATURE.**

</dd> <dt>

*hwndOwner* \[ En\]
</dt> <dd>

Si se requiere una contraseña para cifrar la clave privada, este parámetro es un identificador para el elemento primario del cuadro de diálogo; de lo contrario, es **NULL.**

</dd> <dt>

*pwszKeyName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL para el nombre de la clave que se va a guardar.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Valor **DWORD** que especifica opciones adicionales para la función. Para obtener más información, vea *el parámetro dwFlags* [**en CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ha hecho correctamente, esta función **devuelve TRUE**. La **función PvkPrivateKeySave** devuelve **FALSE** si se produce un error.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
