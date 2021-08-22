---
description: El método Delete elimina un archivo en una ubicación determinada dentro del sistema de archivos de tarjeta inteligente.
ms.assetid: f51b0329-c5dc-4f70-a92e-19dc0dbc55f8
title: Método ISCardFileAccess::D elete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Delete
api_type:
- COM
api_location: ''
ms.openlocfilehash: 721830ea3d446585e7f52c699642b1534c78d34826722b5737e191dfce94c817
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008053"
---
# <a name="iscardfileaccessdelete-method"></a>Método ISCardFileAccess::D elete

\[El **método** Delete está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método Delete** elimina un archivo en una ubicación determinada dentro del sistema de archivos de [*tarjeta*](../secgloss/s-gly.md) inteligente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Delete(
  [in] REFTYPE     refType,
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*refType* \[ En\]
</dt> <dd>

Tipo de referencia usado en *bstrPathSpec.*

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

**TIPO DE SC \_ \_ POR \_ NOMBRE**
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

**TIPO DE SC \_ \_ POR \_ IDENTIFICADOR**
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

**SC \_ TYPE \_ BY \_ SHORT**
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

**SC \_ TYPE \_ BY \_ ANY**
</dt> </dl> </dd> <dt>

*bstrPathSpec* \[ En\]
</dt> <dd>

Identificador del archivo que se va a eliminar.

</dd> <dt>

*flags* \[ En\]
</dt> <dd>

Especifica si se debe usar la mensajería segura y los datos se han preasignado.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**SC \_ FL \_ SECURE \_ MESSAGING**
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

**SC \_ FL \_ PREASIGNADO**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                  | Descripción                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | La operación se completó correctamente.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Parámetro no válido.<br/>                             |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>    | La interfaz no ha implementado este método.<br/> |



 

## <a name="remarks"></a>Comentarios

Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess.**](iscardfileaccess.md)

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Crear**](iscardfileaccess-create.md)
</dt> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
