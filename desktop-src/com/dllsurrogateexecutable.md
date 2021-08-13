---
title: DllSurrogateExecutable
description: Permite que los servidores DLL se ejecuten en un proceso suplente personalizado, junto con el valor del Registro DllSurrogate. Si no se especifica DllSurrogateExecutable, COM pasa NULL como valor para el primer parámetro de la función CreateProcess.
ms.assetid: faf5dde3-bd67-447b-a88c-e8660dc5228e
keywords:
- Valor del Registro DLLSurrogateExecutable COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fc12af22d1f85c2d2e5ff6e75b2904c5fc5eea636a64e314f997ff36a44e38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119373385"
---
# <a name="dllsurrogateexecutable"></a>DllSurrogateExecutable

Permite que los servidores DLL se ejecuten en un proceso suplente personalizado, junto con el valor del Registro [**DllSurrogate.**](dllsurrogate.md) Si **no se especifica DllSurrogateExecutable,** COM pasa **NULL** como valor para el primer parámetro de la [**función CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogateExecutable = file
```

## <a name="remarks"></a>Comentarios

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

 

 