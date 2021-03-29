---
description: El método Seek selecciona el objeto del que se realizará el acceso (lectura y escritura).
ms.assetid: 9e06df70-6415-46dd-b34f-59614d1cbee7
title: 'ISCardFileAccess:: Seek (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Seek
api_type:
- COM
api_location: ''
ms.openlocfilehash: c0d23925ba1c38a05e15bea5e6ee63b3a1c87125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814198"
---
# <a name="iscardfileaccessseek-method"></a>ISCardFileAccess:: Seek (método)

\[El método **Seek** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **Seek** selecciona el objeto del que se realizará el acceso (lectura y escritura).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Seek(
  [in] HSCARD_FILE hFile,
  [in] SEEKTYPE    *Seek,
  [in] LONG        lOffset 
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFile* \[ de\]
</dt> <dd>

Identificador del archivo abierto.

</dd> <dt>

*Buscar* \[ de\]
</dt> <dd>

Ubicación donde debe comenzar la búsqueda.



| Value                                                                                                | Significado                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>SC \_ Buscar \_ desde el \_ principio</dt> </dl> | Comienza la búsqueda al principio.<br/>          |
| <dl> <dt>SC \_ Buscar \_ desde el \_ final </dt> </dl>      | Comience la búsqueda desde el final.<br/>              |
| <dl> <dt>referencia de SC \_ Seek \_ relativa</dt> </dl>        | Comienza la búsqueda desde la posición actual.<br/> |



 

</dd> <dt>

*lOffset* \[ de\]
</dt> <dd>

Número de objetos de datos del objeto de referencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                    |



 

## <a name="remarks"></a>Observaciones

Para leer o escribir en un archivo, llame a [**Read**](iscardfileaccess-read.md) o [**Write**](iscardfileaccess-write.md) , respectivamente.

Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess**](iscardfileaccess.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> <dt>

[**Lectura**](iscardfileaccess-read.md)
</dt> <dt>

[**Escritura**](iscardfileaccess-write.md)
</dt> </dl>

 

 
