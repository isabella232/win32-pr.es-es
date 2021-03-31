---
description: Carga el archivo de recursos de apphelp.
ms.assetid: fca50e00-9324-410a-a572-69441f332593
title: SdbOpenApphelpResourceFile función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpResourceFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2f1dfb1695e25bfb82e01ffa4f9eac4e245a6ffa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423344"
---
# <a name="sdbopenapphelpresourcefile-function"></a>SdbOpenApphelpResourceFile función)

Carga el archivo de recursos de apphelp.

## <a name="syntax"></a>Sintaxis


```C++
HMODULE WINAPI SdbOpenApphelpResourceFile(
  _In_opt_ LPCWSTR pwszACResourceFile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszACResourceFile* \[ en, opcional\]
</dt> <dd>

Ruta de acceso al archivo de recursos. Si este parámetro es **null**, se abre el archivo dll de recursos local.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un identificador al archivo de recursos abierto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




