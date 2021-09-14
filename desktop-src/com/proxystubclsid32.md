---
title: ProxyStubClsid32
description: Mapas un IID a un CLSID en archivos DLL de proxy de 32 bits.
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- ProxyStubClsid32 valor del Registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d1d70ad2deb4f747ecf57fd12f0707ac8b2b9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973629"
---
# <a name="proxystubclsid32"></a>ProxyStubClsid32

Mapas un IID a un CLSID en archivos DLL de proxy de 32 bits.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ SZ reg** que especifica el CLSID para el IID.

Se trata de una entrada necesaria, ya que la asignación de IID a CLSID puede ser diferente para interfaces de 16 y 32 bits. La asignación de IID a CLSID depende de la forma en que los servidores proxy de interfaz se empaquetan en un conjunto de archivos DLL de proxy.

Si agrega interfaces, debe usar esta entrada para registrarlas (sistemas de 32 bits) para que OLE pueda encontrar el código de comunicación remota adecuado para establecer la comunicación entre procesos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)
</dt> <dt>

[**Interfaz**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid**](proxystubclsid.md)
</dt> </dl>

 

 