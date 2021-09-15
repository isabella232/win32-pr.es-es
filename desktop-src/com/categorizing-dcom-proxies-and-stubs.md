---
title: Categorización de servidores proxy y código auxiliar de DCOM
description: Categorización de servidores proxy y código auxiliar de DCOM
ms.assetid: f5d117d6-6c2c-4beb-8869-1581a5b1846f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31685cd1318856b9e305246cfebc2cebb3a7874e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466978"
---
# <a name="categorizing-dcom-proxies-and-stubs"></a>Categorización de servidores proxy y código auxiliar de DCOM

DCOM serializa las referencias a objetos mediante la construcción de objetos OBJREF que contienen CLID. Estos CLSID son vulnerables a ataques de seguridad porque se pueden cargar archivos DLL arbitrarios durante la serialización. Sin embargo, se puede especificar la marca EOAC NO CUSTOM MARSHAL al llamar a \_ \_ \_ [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) (vea [**EOLE \_ AUTHENTICATION \_ CAPABILITIES**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)). Establecer esta marca ayuda a proteger la seguridad del servidor cuando se usa DCOM, ya que reduce las posibilidades de ejecutar archivos DLL arbitrarios. Cuando se establece esta marca, el servidor permite serializar solo los CLID que se implementan en ole32.dll, comadmin.dll, comsvcs.dll o es.dll, o que implementan el identificador de categoría DE \_ SERIALIZADOR CATID.

CATID MARSHALER es un GUID de categoría de componente que se puede asociar a un \_ CLSID que se está serializando de forma personalizada. Las interfaces que se serializan de forma personalizada con este CLSID se permiten cuando EOAC NO CUSTOM MARSHAL se establece a \_ \_ través de \_ [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Categorías del componente](component-categories.md)
</dt> </dl>

 

 