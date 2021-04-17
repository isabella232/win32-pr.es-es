---
title: ProxyStubClsid32
description: Asigna un IID a un CLSID en dll de proxy de 32 bits.
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- Valor del registro ProxyStubClsid32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d1d70ad2deb4f747ecf57fd12f0707ac8b2b9d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359447"
---
# <a name="proxystubclsid32"></a>ProxyStubClsid32

Asigna un IID a un CLSID en dll de proxy de 32 bits.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **reg \_ SZ** que especifica el CLSID para el IID.

Se trata de una entrada necesaria, ya que la asignación de IID a CLSID puede ser diferente para las interfaces de 16 bits y 32 bits. La asignación de IID a CLSID depende de la forma en que los proxies de interfaz se empaquetan en un conjunto de archivos dll de proxy.

Si agrega interfaces, debe usar esta entrada para registrarlas (sistemas de 32 bits) para que OLE pueda encontrar el código remoto adecuado para establecer la comunicación entre procesos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)
</dt> <dt>

[**Interfaz**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid**](proxystubclsid.md)
</dt> </dl>

 

 