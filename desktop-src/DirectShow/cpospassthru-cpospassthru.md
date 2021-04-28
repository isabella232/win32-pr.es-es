---
description: 'Constructor CPosPassThru.CPosPassThru: método constructor.'
ms.assetid: b258401c-158b-4eb8-8736-1e1ad9a8403a
title: Constructor CPosPassThru.CPosPassThru
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CPosPassThru
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2a6c49b305b3c6638aeaaee1480d0b561fd8c99a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085603"
---
# <a name="cpospassthrucpospassthru-constructor"></a>Constructor CPosPassThru.CPosPassThru

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin,
                   
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

Puntero al nombre del objeto para fines de depuración. Asigne este parámetro en memoria estática.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntero al propietario de este objeto. Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación. De lo contrario, establezca este parámetro en **NULL.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a un **valor HRESULT.** ignorado.

</dd> <dt>

*pPin* 
</dt> <dd>

Puntero a la [**interfaz IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin de entrada del filtro.

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



