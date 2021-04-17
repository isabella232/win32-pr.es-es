---
description: Guarda una clave privada y su correspondiente clave pública en un archivo especificado.
ms.assetid: 491a128a-b4aa-4cca-a835-d0e8d7df6720
title: PvkPrivateKeySave función)
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
ms.openlocfilehash: ef60c3f615a704248fbcb8630322fa6b598141ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688036"
---
# <a name="pvkprivatekeysave-function"></a>PvkPrivateKeySave función)

> [!IMPORTANT]
> Esta API está en desuso. Microsoft puede quitar esta API en futuras versiones.

 

La función **PvkPrivateKeySave** guarda una [*clave privada*](../secgloss/p-gly.md) y su correspondiente [*clave pública*](../secgloss/p-gly.md) en un archivo especificado.

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

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

*hCryptProv* \[ de\]
</dt> <dd>

Identificador de un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP).

</dd> <dt>

*hFile* \[ de\]
</dt> <dd>

Identificador de un archivo creado con permisos de lectura y escritura iniciales y permisos de solo lectura posteriores.

</dd> <dt>

*dwKeySpec* \[ de\]
</dt> <dd>

Entero largo para el tipo de clave. Entre los valores posibles se incluyen **en \_ KEYEXCHANGE** o **en la \_ signatura**.

</dd> <dt>

*hwndOwner* \[ de\]
</dt> <dd>

Si se requiere una contraseña para cifrar la clave privada, este parámetro es un identificador del elemento primario del cuadro de diálogo. de lo contrario, es **null**.

</dd> <dt>

*pwszKeyName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null para el nombre de la clave que se va a guardar.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Valor **DWORD** que especifica opciones adicionales para la función. Para obtener más información, vea el parámetro *dwFlags* en [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cuando se realiza correctamente, esta función devuelve **true**. La función **PvkPrivateKeySave** devuelve **false** si se produce un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
