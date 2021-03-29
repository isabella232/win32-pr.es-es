---
description: El método GetFileCapabilities recupera una lista de capacidades de archivo del archivo actual.
ms.assetid: 0d24efd2-d411-4fb3-95c2-4742a58aeb5e
title: 'ISCardFileAccess:: GetFileCapabilities (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetFileCapabilities
api_type:
- COM
api_location: ''
ms.openlocfilehash: ca22f02d327cdfbea527fba3a87f3f149774c091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277535"
---
# <a name="iscardfileaccessgetfilecapabilities-method"></a>ISCardFileAccess:: GetFileCapabilities (método)

\[El método **GetFileCapabilities** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **GetFileCapabilities** recupera una lista de capacidades de archivo del archivo actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFileCapabilities(
  [in, out] LPTLV_TABLE *ppProperties,
  [in, out] LONG        *plProperties,
  [in]      SCARD_FLAGS Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppProperties* \[ in, out\]
</dt> <dd>

Puntero a las estructuras TLV (etiqueta, longitud, valor). En la entrada, este parámetro indica los archivos para los que se van a obtener propiedades. en la salida, este parámetro contiene las propiedades. El ejemplo siguiente es una definición de la estructura TLV.


```C++
#include <windows.h>

typedef struct
{
  DWORD  Tag;
  DWORD  Length;
  BYTE[]  Value;
  BOOL  Valid;
} TLV;
```



Para obtener más información sobre las estructuras TLV, vea [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) .

</dd> <dt>

*plProperties* \[ in, out\]
</dt> <dd>

Puntero al número de entradas de TLV en *ppProperties*.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Especifica si se debe usar la mensajería segura y los datos preasignados.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**\_ \_ mensajería segura de SC FL \_**
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

**SC \_ FL \_ preasignado**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | La operación se completó correctamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                    |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido.<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                        |



 

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

 

 
