---
description: El método Read Lee y devuelve los datos especificados de un archivo determinado.
ms.assetid: 697b8dfa-754b-46cf-ab5c-1ac1d8ae47f2
title: 'ISCardFileAccess:: Read (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: b3d66b5c6e314a4ef7a00a76fabc8660f3bf65eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277019"
---
# <a name="iscardfileaccessread-method"></a>ISCardFileAccess:: Read (método)

\[El método **Read** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **Read** Lee y devuelve los datos especificados de un archivo determinado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Read(
  [in]  HSCARD_FILE  hFile,
  [in]  LONG         *lBytesToRead,
  [in]  SCARD_FLAGS  flags,
  [out] LPBYTEBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFile* \[ de\]
</dt> <dd>

Identificador del archivo abierto al que se va a tener acceso.

</dd> <dt>

*lBytesToRead* \[ de\]
</dt> <dd>

Longitud de los datos que se van a leer (en) o el número de bytes leídos (out). Devuelve una lista de archivos como una matriz de BSTR.

</dd> <dt>

*marcas* \[ de de\]
</dt> <dd>

Especifica si se debe usar la mensajería segura.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**\_ \_ mensajería segura de SC FL \_**
</dt> </dl> </dd> <dt>

*ppBuffer* \[ enuncia\]
</dt> <dd>

Un objeto [**IByteBuffer**](ibytebuffer.md) que contiene los datos leídos.

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

 

 
