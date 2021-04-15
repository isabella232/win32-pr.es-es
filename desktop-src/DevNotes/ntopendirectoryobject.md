---
description: Abre un objeto de directorio existente.
ms.assetid: 7313fb32-976b-4c73-b9ba-09fb8ad7faf1
title: NtOpenDirectoryObject función)
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
ms.openlocfilehash: ceea03c36e0617e2f48887275e7867e3589c87ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649585"
---
# <a name="ntopendirectoryobject-function"></a>NtOpenDirectoryObject función)

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

*DirectoryHandle* \[ enuncia\]
</dt> <dd>

Identificador del objeto de directorio recién abierto.

</dd> <dt>

*DesiredAccess* \[ de\]
</dt> <dd>

Una [**\_ máscara de acceso**](../secauthz/access-mask.md) que especifica el acceso solicitado al objeto de directorio. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                                                                                      | Significado                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="DIRECTORY_QUERY"></span><span id="directory_query"></span><dl> <dt>**Directorio \_ de CONSULTA**</dt> <dt>0x0001</dt> </dl>                                            | Consultar el acceso al objeto de directorio.<br/>                            |
| <span id="DIRECTORY_TRAVERSE"></span><span id="directory_traverse"></span><dl> <dt>**Directorio \_ de ATRAVESAR**</dt> <dt>0x0002</dt> </dl>                                   | Nombre: acceso de búsqueda al objeto de directorio.<br/>                      |
| <span id="DIRECTORY_CREATE_OBJECT"></span><span id="directory_create_object"></span><dl> <dt>**Directorio \_ de CREAR \_ objeto**</dt> <dt>0x0004</dt> </dl>                   | Acceso de creación de nombre al objeto de directorio.<br/>                    |
| <span id="DIRECTORY_CREATE_SUBDIRECTORY"></span><span id="directory_create_subdirectory"></span><dl> <dt>**Directorio \_ de CREAR \_ SUBdirectorio**</dt> <dt>0x0008</dt> </dl> | Subdirectorio: acceso de creación al objeto de directorio.<br/>            |
| <span id="DIRECTORY_ALL_ACCESS"></span><span id="directory_all_access"></span><dl> <dt>**Directorio \_ de Todos \_ los**</dt> derechos de acceso <dt>estándar \_ \_ requeridos \| 0xF</dt> </dl> | Todos los derechos anteriores y los **\_ derechos estándar \_ necesarios**.<br/> |



 

</dd> <dt>

*ObjectAttributes* \[ de\]
</dt> <dd>

Atributos del objeto de directorio. Para inicializar la estructura de **\_ atributos de objeto** , use la macro **InitializeObjectAttributes** . Para obtener más información, consulte la documentación de estos elementos en la documentación del WDK.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve el estado \_ correcto o un estado de error. Los códigos de estado posibles son los siguientes.



| Código devuelto                                                                                                       | Descripción                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Estado de \_ recursos insuficientes \_**</dt> </dl>    | No se pudo asignar un búfer temporal requerido por esta función.<br/>                                                                                                                                                                                                                           |
| <dl> <dt>**ESTADO \_ parámetro no válido \_**</dt> </dl>         | El parámetro ObjectAttributes especificado era un puntero **nulo** , no un puntero válido a una estructura de **\_ atributos de objeto** o algunos de los miembros especificados en la estructura de **\_ atributos de objeto** no eran válidos.<br/>                                                                          |
| <dl> <dt>**nombre del objeto de estado \_ \_ \_ no válido**</dt> </dl>      | El parámetro *ObjectAttributes* contenía un miembro **objectname** en la estructura de **\_ atributos de objeto** que no era válida porque se encontró una cadena vacía después del carácter **\_ \_ \_ separador de ruta de acceso de nombre de objeto** .<br/>                                                                        |
| <dl> <dt>**nombre del objeto de estado \_ \_ \_ no \_ encontrado**</dt> </dl>   | El parámetro *ObjectAttributes* contenía un miembro **objectname** en la estructura de **\_ atributos de objeto** que no se pudo encontrar.<br/>                                                                                                                                                           |
| <dl> <dt>**Ruta de acceso del objeto de estado \_ \_ \_ no \_ encontrada**</dt> </dl>   | El parámetro *ObjectAttributes* contenía un miembro **objectname** en la estructura de **\_ atributos de objeto** con una ruta de acceso de objeto que no se pudo encontrar. <br/>                                                                                                                                      |
| <dl> <dt>**Estado \_ de Sintaxis de ruta de objeto \_ \_ \_ incorrecta**</dt> </dl> | El parámetro *ObjectAttributes* no contenía un miembro **RootDirectory** , pero el miembro **objectname** de la estructura de **\_ atributos de objeto** era una cadena vacía o no contenía un carácter **\_ \_ \_ separador de ruta de acceso de nombre de objeto** . Esto indica una sintaxis incorrecta para la ruta de acceso del objeto.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**NtQueryDirectoryObject**](ntquerydirectoryobject.md)
</dt> </dl>

 

 
