---
description: El método Seek selecciona el objeto desde el que se realizará el acceso (lectura/escritura).
ms.assetid: 9e06df70-6415-46dd-b34f-59614d1cbee7
title: Método ISCardFileAccess::Seek
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
ms.openlocfilehash: 5f4059eb2943411cfa5a3fb2b2ae247cd0fda7dd735cc1f1f61d516181976b6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923164"
---
# <a name="iscardfileaccessseek-method"></a>Método ISCardFileAccess::Seek

\[El **método Seek** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método Seek** selecciona el objeto desde el que se realizará el acceso (lectura/escritura).

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

*hFile* \[ En\]
</dt> <dd>

Identificador del archivo abierto.

</dd> <dt>

*Buscar* \[ En\]
</dt> <dd>

Ubicación donde debe comenzar la búsqueda.



| Valor                                                                                                | Significado                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>SC \_ SEEK DESDE EL \_ \_ PRINCIPIO</dt> </dl> | Comience la búsqueda al principio.<br/>          |
| <dl> <dt>SC \_ SEEK \_ FROM \_ END </dt> </dl>      | Comience la búsqueda desde el final.<br/>              |
| <dl> <dt>SC \_ SEEK \_ RELATIVE</dt> </dl>        | Comience la búsqueda desde la posición actual.<br/> |



 

</dd> <dt>

*lOffset* \[ En\]
</dt> <dd>

Número de objetos de datos del objeto de referencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                    |



 

## <a name="remarks"></a>Comentarios

Para leer o escribir desde un archivo, llame a [**Lectura**](iscardfileaccess-read.md) o [**Escritura**](iscardfileaccess-write.md) respectivamente.

Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess.**](iscardfileaccess.md)

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> <dt>

[**Lectura**](iscardfileaccess-read.md)
</dt> <dt>

[**Escritura**](iscardfileaccess-write.md)
</dt> </dl>

 

 
