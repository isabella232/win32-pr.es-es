---
description: Recupera los atributos básicos del objeto de archivo especificado.
ms.assetid: 19f9a2ac-4db6-4c67-9f85-c107063e11b8
title: NtQueryAttributesFile función)
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
ms.openlocfilehash: a1d6d2ff20539f5ef65c0886ba51a0dbabafb44d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670626"
---
# <a name="ntqueryattributesfile-function"></a>NtQueryAttributesFile función)

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

*ObjectAttributes* \[ de\]
</dt> <dd>

Puntero a una estructura [de \_ atributos de objeto](https://msdn.microsoft.com/library/aa491657.aspx) que proporciona los atributos que se van a utilizar para el objeto de archivo.

</dd> <dt>

*FileInformation* \[ enuncia\]
</dt> <dd>

Puntero a una estructura [de \_ \_ información básica de archivo](https://msdn.microsoft.com/library/aa491634.aspx) para recibir la información de atributo de archivo devuelta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un código de error NTSTATUS o.

Los formularios y la importancia de los códigos de error de NTSTATUS se enumeran en el archivo de encabezado NTSTATUS. h disponible en el WDK y se describen en la documentación de WDK.

## <a name="remarks"></a>Observaciones

Esta función no tiene ningún archivo de encabezado asociado. La biblioteca de importación asociada, ntdll. lib, está disponible en el WDK. También puede utilizar las funciones [**LoadLibrary**](-loadlibrary.md) y [**GetProcAddress**](-getprocaddress-.md) para vincular dinámicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 




