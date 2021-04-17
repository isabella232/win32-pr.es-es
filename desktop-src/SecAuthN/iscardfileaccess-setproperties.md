---
description: El método SetProperties establece el primitivo al que se refiere TLVs (etiqueta, longitud, valor) para el objeto especificado.
ms.assetid: f8f75c8e-14f4-4bc4-b49d-b232ede374b0
title: 'ISCardFileAccess:: SetProperties (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.SetProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: b54c2193ec17bca9f9b3ba00b2c2bc133707dbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652577"
---
# <a name="iscardfileaccesssetproperties-method"></a>ISCardFileAccess:: SetProperties (método)

\[El método **SetProperties** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **SetProperties** establece el primitivo al que se refiere TLVs (etiqueta, longitud, valor) para el objeto especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetProperties(
  [in] REFTYPE     refType,
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags,
  [in] LPTLV_TABLE pTable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*refType* \[ de\]
</dt> <dd>

Tipo de referencia que se usa en *bstrPathSpec*.

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

**\_tipo SC \_ por \_ nombre**
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

**\_tipo SC \_ por \_ identificador**
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

**\_tipo SC \_ por \_ corto**
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

**\_tipo SC \_ por \_ cualquier**
</dt> </dl> </dd> <dt>

*bstrPathSpec* \[ de\]
</dt> <dd>

Archivo:

</dd> <dt>

*marcas* \[ de de\]
</dt> <dd>

Especifica si se debe usar la mensajería segura.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**\_ \_ mensajería segura de SC FL \_**
</dt> </dl> </dd> <dt>

*pTable* \[ de\]
</dt> <dd>

Puntero a las estructuras TLV cuyo valor se debe establecer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                    |



 

## <a name="remarks"></a>Observaciones

Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess**](iscardfileaccess.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

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
</dt> </dl>

 

 
