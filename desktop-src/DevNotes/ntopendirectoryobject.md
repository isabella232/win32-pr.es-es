---
description: Abre un objeto de directorio existente.
ms.assetid: 7313fb32-976b-4c73-b9ba-09fb8ad7faf1
title: Función NtOpenDirectoryObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: ddfe43bab114af968de76673f08f2e301f775e2e7475e7b17a2e08004ef50dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003796"
---
# <a name="ntopendirectoryobject-function"></a>Función NtOpenDirectoryObject

\[Esta función puede modificarse o no estar disponible en el futuro.\]

Abre un objeto de directorio existente.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI NtOpenDirectoryObject(
  _Out_ PHANDLE            DirectoryHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DirectoryHandle* \[ out\]
</dt> <dd>

Identificador del objeto de directorio recién abierto.

</dd> <dt>

*DesiredAccess* \[ En\]
</dt> <dd>

Máscara [**de \_ acceso**](../secauthz/access-mask.md) que especifica el acceso solicitado al objeto de directorio. Este parámetro puede ser uno o varios de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                      | Significado                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="DIRECTORY_QUERY"></span><span id="directory_query"></span><dl> <dt>**DIRECTORIO \_ Consulta**</dt> <dt>0x0001</dt> </dl>                                            | Consulta el acceso al objeto de directorio.<br/>                            |
| <span id="DIRECTORY_TRAVERSE"></span><span id="directory_traverse"></span><dl> <dt>**DIRECTORY \_ Recorrer**</dt> <dt>0x0002</dt> </dl>                                   | Acceso de búsqueda de nombres al objeto de directorio.<br/>                      |
| <span id="DIRECTORY_CREATE_OBJECT"></span><span id="directory_create_object"></span><dl> <dt>**DIRECTORY \_ Create \_ OBJECT**</dt> <dt>0x0004</dt> </dl>                   | Acceso de creación de nombres al objeto de directorio.<br/>                    |
| <span id="DIRECTORY_CREATE_SUBDIRECTORY"></span><span id="directory_create_subdirectory"></span><dl> <dt>**DIRECTORY \_ Create \_ SUBDIRECTORY**</dt> <dt>0x0008</dt> </dl> | Acceso de creación de subdirectorios al objeto de directorio.<br/>            |
| <span id="DIRECTORY_ALL_ACCESS"></span><span id="directory_all_access"></span><dl> <dt>**DIRECTORIO \_ TODOS \_ LOS DERECHOS**</dt> ESTÁNDAR DE ACCESO NECESARIOS <dt> \_ \_ \| 0xF</dt> </dl> | Todos los derechos anteriores más **LOS DERECHOS \_ ESTÁNDAR \_ REQUERIDOS.**<br/> |



 

</dd> <dt>

*ObjectAttributes* \[ En\]
</dt> <dd>

Atributos del objeto de directorio. Para inicializar **la estructura OBJECT \_ ATTRIBUTES,** use la macro **InitializeObjectAttributes.** Para obtener más información, consulte la documentación de estos elementos en la documentación de WDK.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve STATUS \_ SUCCESS o un estado de error. Los códigos de estado posibles incluyen lo siguiente.



| Código devuelto                                                                                                       | Descripción                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**RECURSOS \_ INSUFICIENTES \_ DE ESTADO**</dt> </dl>    | No se pudo asignar un búfer temporal requerido por esta función.<br/>                                                                                                                                                                                                                           |
| <dl> <dt>**PARÁMETRO STATUS \_ INVALID \_**</dt> </dl>         | El parámetro ObjectAttributes especificado era un puntero **NULL,** no un puntero válido a una estructura **OBJECT \_ ATTRIBUTES** o algunos de los miembros especificados en la estructura **OBJECT \_ ATTRIBUTES** no eran válidos.<br/>                                                                          |
| <dl> <dt>**NOMBRE DE \_ OBJETO DE ESTADO NO \_ \_ VÁLIDO**</dt> </dl>      | El *parámetro ObjectAttributes* contenía un miembro **ObjectName** en la estructura **OBJECT \_ ATTRIBUTES** que no era válido porque se encontró una cadena vacía después del carácter SEPARADOR PATH DE NOMBRE **\_ \_ \_ DE** OBJETO.<br/>                                                                        |
| <dl> <dt>**NOMBRE DEL \_ OBJETO DE ESTADO NO \_ \_ \_ ENCONTRADO**</dt> </dl>   | El *parámetro ObjectAttributes* contenía un **miembro ObjectName** en la estructura **OBJECT \_ ATTRIBUTES** que no se encontró.<br/>                                                                                                                                                           |
| <dl> <dt>**RUTA DE \_ ACCESO DEL OBJETO DE ESTADO NO \_ \_ \_ ENCONTRADA**</dt> </dl>   | El *parámetro ObjectAttributes* contenía un **miembro ObjectName** en la estructura **OBJECT \_ ATTRIBUTES** con una ruta de acceso de objeto que no se encontró. <br/>                                                                                                                                      |
| <dl> <dt>**STATUS \_ SINTAXIS INCORRECTA \_ DE RUTA DE ACCESO DE \_ \_ OBJETO**</dt> </dl> | El *parámetro ObjectAttributes* no contenía un miembro **RootDirectory,** pero el miembro **ObjectName** de la estructura **OBJECT \_ ATTRIBUTES** era una cadena vacía o no contenía un carácter SEPARADOR DE RUTA DE ACCESO DE NOMBRE **\_ \_ \_ DE** OBJETO. Esto indica una sintaxis incorrecta para la ruta de acceso del objeto.<br/> |



 

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**NtQueryDirectoryObject**](ntquerydirectoryobject.md)
</dt> </dl>

 

 
