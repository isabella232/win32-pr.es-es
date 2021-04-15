---
description: Esta API está pensada solo para uso interno y no debe usarse en el código.
ms.assetid: 836A7515-8C22-4032-9E99-F89B32C21685
title: Función ApiSetQueryApiSetPresence (Apiquery. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApiSetQueryApiSetPresence
api_type:
- DllExport
api_location:
- api-ms-win-core-apiquery-l1-1-0.dll
- ntdll.dll
ms.openlocfilehash: 738a69b0d08f7e619dbd64229d0c13b2ae7dfaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669980"
---
# <a name="apisetqueryapisetpresence-function"></a>ApiSetQueryApiSetPresence función)

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Esta API está pensada solo para uso interno y no debe usarse en el código.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI ApiSetQueryApiSetPresence(
  _In_  PCUNICODE_STRING Namespace,
  _Out_ PBOOLEAN         Present
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Espacio de nombres* \[ de\]
</dt> <dd></dd> <dt>

*Presente* \[ enuncia\]
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                                                                                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                                                                                                                  |
| Encabezado<br/>                   | <dl> <dt>Apiquery. h</dt> </dl>                                                                                                                 |
| Biblioteca<br/>                  | <dl> <dt>API-MS-WIN-Core-apiquery-L1. lib; </dt> <dt>API-MS-WIN-Core-apiquery-L1-1 -0. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt> </dl>                                                                                        |



 

 




