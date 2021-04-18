---
title: DllSurrogateExecutable
description: Permite que los servidores DLL se ejecuten en un proceso suplente personalizado, junto con el valor del registro DllSurrogate. Si no se especifica DllSurrogateExecutable, COM pasa NULL como el valor para el primer parámetro de la función CreateProcess.
ms.assetid: faf5dde3-bd67-447b-a88c-e8660dc5228e
keywords:
- Valor del registro DllSurrogateExecutable COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877297673b0a518006ecf903f447984f9023da34
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105705049"
---
# <a name="dllsurrogateexecutable"></a>DllSurrogateExecutable

Permite que los servidores DLL se ejecuten en un proceso suplente personalizado, junto con el valor del registro [**DllSurrogate**](dllsurrogate.md) . Si no se especifica **DllSurrogateExecutable** , com pasa **null** como el valor para el primer parámetro de la función [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogateExecutable = file
```

## <a name="remarks"></a>Observaciones

Este valor es de tipo **reg \_ SZ**. Funciona junto con el valor [**DllSurrogate**](dllsurrogate.md) para evitar cualquier ambigüedad al utilizar la función [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) . **DllSurrogate** indica si es necesario usar un suplente personalizado y esta información se pasa como el primer parámetro de **CreateProcess**. Dependiendo de la implementación de **CreateProcess**, esta información puede ser ambigua. Si se especifica **DllSurrogateExecutable** , com pasa el valor como primer parámetro de **CreateProcess**. Si no se especifica **DllSurrogateExecutable** , com pasa **null** como el valor para el primer parámetro de **CreateProcess**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[Suplentes DLL](dll-surrogates.md)
</dt> <dt>

[**DllSurrogate**](dllsurrogate.md)
</dt> <dt>

[**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 