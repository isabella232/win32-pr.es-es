---
title: ProxyStubClsid
description: Mapas un IID a un CLSID en archivos DLL de proxy de 16 bits.
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- Valor del Registro ProxyStubClsid COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f86db768979a72d2d2f0b8c7a137d6b105f4a52d082ec50c6e78ba271fbca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129997"
---
# <a name="proxystubclsid"></a>ProxyStubClsid

Mapas un IID a un CLSID en archivos DLL de proxy de 16 bits.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ SZ reg** que especifica el CLSID para el IID.

Si agrega interfaces, debe usar esta entrada para registrarlas (sistemas de 16 bits) para que OLE pueda encontrar el código de comunicación remota adecuado para establecer la comunicación entre procesos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid32**](proxystubclsid32.md)
</dt> </dl>

 

 




