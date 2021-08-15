---
description: El método Write escribe datos en un archivo abierto actual.
ms.assetid: 0c92af34-a9db-4242-8b6e-d1010a0d7afa
title: MÉTODO ISCardFileAccess::Write
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: c48f900ad5026af61cfc5b4f68c7908bd77881a637082a3fe1d05bc7c72f4b51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923184"
---
# <a name="iscardfileaccesswrite-method"></a>MÉTODO ISCardFileAccess::Write

\[El **método Write** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método Write** escribe datos en un archivo abierto actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Write(
  [in] HSCARD_FILE  hFile,
  [in] LPBYTEBUFFER pData,
  [in] SCARD_FLAGS  flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFile* \[ En\]
</dt> <dd>

Identificador de un archivo abierto.

</dd> <dt>

*pData* \[ En\]
</dt> <dd>

Objeto o datos que se escribirán.

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
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Se pasó un puntero no válido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                    |



 

## <a name="remarks"></a>Comentarios

Para abrir o cerrar un archivo, llame a [**Abrir**](iscardfileaccess-open.md) [**o Cerrar**](iscardfileaccess-close.md), respectivamente.

Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess.**](iscardfileaccess.md)

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de [*error*](../secgloss/s-gly.md) de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Cerrar**](iscardfileaccess-close.md)
</dt> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> <dt>

[**Abierto**](iscardfileaccess-open.md)
</dt> </dl>

 

 
