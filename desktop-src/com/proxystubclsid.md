---
title: ProxyStubClsid
description: Mapas un IID a un CLSID en archivos DLL de proxy de 16 bits.
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- Valor del Registro ProxyStubClsid COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adfbe319903b2e278be342d169a2e523c952693
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369591"
---
# <a name="proxystubclsid"></a>ProxyStubClsid

Mapas un IID a un CLSID en archivos DLL de proxy de 16 bits.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG SZ** que especifica el CLSID para el IID.

Si agrega interfaces, debe usar esta entrada para registrarlas (sistemas de 16 bits) para que OLE pueda encontrar el código de comunicación remota adecuado para establecer la comunicación entre procesos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid32**](proxystubclsid32.md)
</dt> </dl>

 

 




