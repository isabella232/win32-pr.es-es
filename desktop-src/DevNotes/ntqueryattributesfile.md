---
description: Recupera los atributos básicos del objeto de archivo especificado.
ms.assetid: 19f9a2ac-4db6-4c67-9f85-c107063e11b8
title: Función NtQueryAttributesFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryAttributesFile
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: e6b1ecdc7cc7f0a5c18afc3eeb613c3f9cd9a38aa22a876ad156c3d1c6b1bc97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826811"
---
# <a name="ntqueryattributesfile-function"></a>Función NtQueryAttributesFile

\[Esta función se puede cambiar o quitar de Windows sin previo aviso.\]

Recupera los atributos básicos del objeto de archivo especificado.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS NtQueryAttributesFile(
  _In_  POBJECT_ATTRIBUTES      ObjectAttributes,
  _Out_ PFILE_BASIC_INFORMATION FileInformation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ObjectAttributes* \[ En\]
</dt> <dd>

Puntero a una estructura [OBJECT \_ ATTRIBUTES](https://msdn.microsoft.com/library/aa491657.aspx) que proporciona los atributos que se usarán para el objeto de archivo.

</dd> <dt>

*FileInformation* \[ out\]
</dt> <dd>

Puntero a una estructura [FILE \_ BASIC \_ INFORMATION](https://msdn.microsoft.com/library/aa491634.aspx) para recibir la información de atributo de archivo devuelta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un NTSTATUS o un código de error.

Los formatos y la importancia de los códigos de error NTSTATUS se enumeran en el archivo de encabezado Ntstatus.h disponible en WDK y se describen en la documentación de WDK.

## <a name="remarks"></a>Comentarios

Esta función no tiene ningún archivo de encabezado asociado. La biblioteca de importación asociada, Ntdll.lib, está disponible en WDK. También puede usar las funciones [**LoadLibrary**](-loadlibrary.md) y [**GetProcAddress**](-getprocaddress-.md) para vincular dinámicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 




