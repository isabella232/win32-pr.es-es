---
description: Enumera los archivos protegidos.
ms.assetid: 46a1ff83-afed-4ce3-bb62-551446efdb78
title: Función SfcGetFiles (sfcfiles. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910594"
---
# <a name="sfcgetfiles-function"></a>SfcGetFiles función)

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. Se ha quitado la compatibilidad con esta función en Windows Vista y Windows Server 2008. En su lugar, use las funciones admitidas que se enumeran en [las funciones de WRP](wfp-functions.md) .\]

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

*ProtFileData* \[ enuncia\]
</dt> <dd>

Puntero a una estructura [**de \_ \_ entrada de archivo PPROTECT**](pprotect-file-entry.md) que contiene la lista de archivos protegidos.

</dd> <dt>

*FileCount* \[ enuncia\]
</dt> <dd>

Puntero a una ubicación que contiene un valor ULONG que es el número de archivos protegidos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es STATUs \_ Success. Si se produce un error en la función, devuelve el código de error NTSTATUS adecuado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Sfcfiles. h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Sfcfiles.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_entrada de archivo PPROTECT \_**](pprotect-file-entry.md)
</dt> </dl>

 

 




