---
description: Hace que el archivo especificado (EF o DF) no sea válido. Otros métodos no pueden tener acceso a un archivo que no es válido antes de usar Volver a usar.
ms.assetid: 5600fcf0-091c-437e-a45c-4de5b0a47d68
title: MÉTODO ISCardFileAccess::Invalidate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Invalidate
api_type:
- COM
api_location: ''
ms.openlocfilehash: d0d1ed7aa9bbe69f67c0e4e4b4952e23fbfa75bfca470395d9a36eb6867ab16b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481102"
---
# <a name="iscardfileaccessinvalidate-method"></a>MÉTODO ISCardFileAccess::Invalidate

\[El **método Invalidate** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método Invalidate** hace que el archivo especificado (EF o DF) no sea válido. Otros métodos no pueden tener acceso a un archivo que no es válido antes de usar [**Volver a usar**](iscardfileaccess-rehabilitate.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Invalidate(
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrPathSpec* \[ En\]
</dt> <dd>

Archivo:

</dd> <dt>

*flags* \[ En\]
</dt> <dd>

Especifica si se debe usar la mensajería segura.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**MENSAJERÍA SEGURA DE SC \_ FL \_ \_**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Un parámetro no es válido.<br/>         |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Se pasó un puntero no válido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                    |



 

## <a name="remarks"></a>Observaciones

Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess.**](iscardfileaccess.md)

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de [*error*](../secgloss/s-gly.md) de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> <dt>

[**Rehabilitar**](iscardfileaccess-rehabilitate.md)
</dt> </dl>

 

 
