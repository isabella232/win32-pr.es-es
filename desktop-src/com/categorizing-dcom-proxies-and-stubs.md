---
title: Categorización de servidores proxy y código auxiliar de DCOM
description: Categorización de servidores proxy y código auxiliar de DCOM
ms.assetid: f5d117d6-6c2c-4beb-8869-1581a5b1846f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45f61d89e31316975685d3e603a93d30559546c86abc3b63e8e7e8a0c83ff1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310872"
---
# <a name="categorizing-dcom-proxies-and-stubs"></a>Categorización de servidores proxy y código auxiliar de DCOM

DCOM serializa las referencias a objetos mediante la construcción de objetos OBJREF que contienen CLID. Estos CLSID son vulnerables a ataques de seguridad porque se pueden cargar archivos DLL arbitrarios durante la serialización. Sin embargo, se puede especificar la marca EOAC NO CUSTOM MARSHAL al llamar a \_ \_ \_ [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) (vea [**EOLE \_ AUTHENTICATION \_ CAPABILITIES**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)). Establecer esta marca ayuda a proteger la seguridad del servidor cuando se usa DCOM, ya que reduce las posibilidades de ejecutar archivos DLL arbitrarios. Cuando se establece esta marca, el servidor permite serializar solo los CLID que se implementan en ole32.dll, comadmin.dll, comsvcs.dll o es.dll, o que implementan el identificador de categoría DE \_ SERIALIZADOR CATID.

CATID MARSHALER es un GUID de categoría de componente que se puede asociar a un \_ CLSID que se está serializando de forma personalizada. Las interfaces que se serializan de forma personalizada con este CLSID se permiten cuando EOAC NO CUSTOM MARSHAL se establece a través \_ \_ de \_ [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Categorías del componente](component-categories.md)
</dt> </dl>

 

 