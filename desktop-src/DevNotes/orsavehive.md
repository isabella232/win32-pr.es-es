---
description: Escribe el subárbol del registro sin conexión especificado en un archivo.
ms.assetid: 26f2eed9-e6e0-4dc0-8b91-212cde072744
title: Función ORSaveHive (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSaveHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 59df5b191a9bc0cfe98e1681665c5814935aa2c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649545"
---
# <a name="orsavehive-function"></a>ORSaveHive función)

Escribe el subárbol del registro sin conexión especificado en un archivo.

## <a name="syntax"></a>Sintaxis


```C++
DWORD ORSaveHive(
  _In_ ORHKEY Handle,
  _In_ PCWSTR lpHivePath,
  _In_ DWORD  dwOsMajorVersion,
  _In_ DWORD  dwOsMinorVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Identificador* \[ de de\]
</dt> <dd>

Identificador del subárbol del registro sin conexión que se va a guardar.

</dd> <dt>

*lpHivePath* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode que especifica el nombre del archivo de subárbol del registro. Este no puede ser el nombre de un archivo existente.

</dd> <dt>

*dwOsMajorVersion* \[ de\]
</dt> <dd>

Número de versión principal del sistema operativo. Este miembro puede ser uno de los valores siguientes.



| Value                                                                        | Significado                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>5</dt> </dl> | Si *dwOsMinorVersion* es 1, el sistema operativo es Windows XP.<br/> Si *dwOsMinorVersion* es 2, el sistema operativo es windows Server 2003 R2, windows Server 2003 o Windows XP Professional x64 Edition.<br/> |
| <dl> <dt>6</dt> </dl> | Si *dwOsMinorVersion* es 0, el sistema operativo es windows Server 2008 o Windows Vista.<br/> Si *dwOsMinorVersion* es 1, el sistema operativo es windows Server 2008 R2 o Windows 7.<br/>                       |



 

</dd> <dt>

*dwOsMinorVersion* \[ de\]
</dt> <dd>

Número de versión secundaria del sistema operativo. Este miembro puede ser uno de los valores siguientes.



| Value                                                                        | Significado                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Si *dwOsMajorVersion* es 6, el sistema operativo es windows Server 2008 o Windows Vista.<br/>                                                                                                                                          |
| <dl> <dt>1</dt> </dl> | Si *dwOsMajorVersion* es 5, el sistema operativo es Windows XP.<br/> Si *dwOsMajorVersion* es 6, el sistema operativo es windows Server 2008 R2 o Windows 7.<br/>                                                                |
| <dl> <dt>2</dt> </dl> | Si *dwOsMajorVersion* es 5, el sistema operativo es windows Server 2003 R2, windows Server 2003 o Windows XP Professional x64 Edition. <br/> Si *dwOsMajorVersion* es 6, el parámetro *dwOsMinorVersion* debe ser 0 o 1. <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error. Entre los posibles códigos de error se incluyen los siguientes:

-   Si el autor de la llamada no tiene los derechos de acceso necesarios para escribir el archivo, la función devuelve el ERROR \_ acceso \_ denegado.
-   Si el archivo especificado ya existe, la función devuelve el ERROR \_ ya \_ existe.

## <a name="remarks"></a>Observaciones

La función **ORSaveHive** se debe usar para guardar los cambios realizados en un subárbol del registro sin conexión. Los cambios no se conservan hasta que se llama a **ORSaveHive** para guardar el subárbol en un archivo.

Los parámetros *dwOsMajorVersion* y *dwOsMinorVersion* especifican el formato de destino del archivo de subárbol del registro. En la tabla siguiente se resumen los números de versión más recientes del sistema operativo.



| Sistema operativo                    | Número de versión |
|-------------------------------------|----------------|
| Windows Server 2008 R2              | 6.1            |
| Windows 7                           | 6.1            |
| Windows Server 2008                 | 6.0            |
| Windows Vista                       | 6.0            |
| Windows Server 2003 R2              | 5.2            |
| Windows Server 2003                 | 5.2            |
| Windows XP Professional x64 Edition | 5.2            |
| Windows XP                          | 5,1            |



 

Utilice la función [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) para recuperar información sobre el sistema operativo actual.

La función **ORSaveHive** bloquea el subárbol del registro mientras escribe el subárbol en el archivo, cierra el archivo y libera el bloqueo. El subárbol del registro permanece en memoria hasta que se cierra mediante una llamada a la función [**ORCloseHive**](orclosehive.md) . Es posible realizar más cambios en el subárbol del registro mientras está abierto; sin embargo, para conservar estos cambios, el Hive debe guardarse en un archivo nuevo, ya que la función **ORSaveHive** no sobrescribirá un archivo existente.

La función **ORSaveHive** se puede usar para guardar parte del subárbol del registro sin conexión. La clave especificada en el parámetro *Handle* se convierte en la clave raíz de un subárbol que consta de la clave especificada y todas sus subclaves.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows offline Registry Library versión 1,0 o posterior<br/>                      |
| Encabezado<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| Archivo DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> <dt>

[**ORCloseHive**](orclosehive.md)
</dt> <dt>

[**OROpenHive**](oropenhive.md)
</dt> </dl>

 

 
