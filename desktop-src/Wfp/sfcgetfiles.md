---
description: Enumera los archivos protegidos.
ms.assetid: 46a1ff83-afed-4ce3-bb62-551446efdb78
title: Función SfcGetFiles (Sfcfiles.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SfcGetFiles
api_type:
- DllExport
api_location:
- Sfcfiles.dll
ms.openlocfilehash: 6b38b761372db656308e778fd96ea48607cf1f21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359857"
---
# <a name="sfcgetfiles-function"></a>Función SfcGetFiles

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. Se quitó la compatibilidad con esta función en Windows Vista y Windows Server 2008. En su lugar, use las funciones admitidas [enumeradas en Funciones de WRP.](wfp-functions.md)\]

Enumera los archivos protegidos.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI SfcGetFiles(
  _Out_ PPROTECT_FILE_ENTRY ProtFileData,
  _Out_ PULONG              FileCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProtFileData* \[ out\]
</dt> <dd>

Puntero a una estructura [**PPROTECT \_ FILE \_ ENTRY**](pprotect-file-entry.md) que contiene la lista de archivos protegidos.

</dd> <dt>

*FileCount* \[ out\]
</dt> <dd>

Puntero a una ubicación que contiene un valor ULONG que es el número de archivos protegidos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es STATUS \_ SUCCESS. Si se produce un error en la función, devuelve el código de error NTSTATUS adecuado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Sfcfiles.h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Sfcfiles.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ENTRADA DE ARCHIVO PPROTECT \_ \_**](pprotect-file-entry.md)
</dt> </dl>

 

 




