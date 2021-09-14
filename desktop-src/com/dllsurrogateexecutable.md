---
title: DllSurrogateExecutable
description: Permite que los servidores DLL se ejecuten en un proceso suplente personalizado, junto con el valor del Registro DllSurrogate. Si no se especifica DllSurrogateExecutable, COM pasa NULL como valor para el primer parámetro de la función CreateProcess.
ms.assetid: faf5dde3-bd67-447b-a88c-e8660dc5228e
keywords:
- DllSurrogateExecutable registry value COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877297673b0a518006ecf903f447984f9023da34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359383"
---
# <a name="dllsurrogateexecutable"></a>DllSurrogateExecutable

Permite que los servidores DLL se ejecuten en un proceso suplente personalizado, junto con el valor del Registro [**DllSurrogate.**](dllsurrogate.md) Si **no se especifica DllSurrogateExecutable,** COM pasa **NULL** como valor para el primer parámetro de la [**función CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogateExecutable = file
```

## <a name="remarks"></a>Observaciones

Este valor es de tipo **REG \_ SZ.** Funciona junto con el valor [**DllSurrogate**](dllsurrogate.md) para evitar cualquier ambigüedad al usar la [**función CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) **DllSurrogate** indica si es necesario usar un suplente personalizado y esta información se pasa como primer parámetro **para CreateProcess.** En función de la implementación **de CreateProcess,** esta información puede ser ambigua. Si **se especifica DllSurrogateExecutable,** COM pasa el valor como primer parámetro de **CreateProcess.** Si **no se especifica DllSurrogateExecutable,** COM pasa **NULL** como valor para el primer parámetro **de CreateProcess.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[Suplentes de DLL](dll-surrogates.md)
</dt> <dt>

[**DllSurrogate**](dllsurrogate.md)
</dt> <dt>

[**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 