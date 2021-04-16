---
title: Categorización de proxies y códigos auxiliares de DCOM
description: Categorización de proxies y códigos auxiliares de DCOM
ms.assetid: f5d117d6-6c2c-4beb-8869-1581a5b1846f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31685cd1318856b9e305246cfebc2cebb3a7874e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105714479"
---
# <a name="categorizing-dcom-proxies-and-stubs"></a>Categorización de proxies y códigos auxiliares de DCOM

DCOM calcula las referencias a los objetos mediante la construcción de OBJREFs que contienen CLSID. Estos CLSID son vulnerables a los ataques de seguridad porque se pueden cargar archivos dll arbitrarios durante el cálculo de referencias. Sin embargo, \_ \_ \_ se puede especificar la marca de serialización no personalizada EOAC al llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) (consulte [**capacidades de \_ autenticación \_ de Eole**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)). La configuración de esta marca ayuda a proteger la seguridad del servidor al usar DCOM porque reduce las posibilidades de ejecutar archivos dll arbitrarios. Cuando se establece esta marca, el servidor permite el cálculo de referencias solo de los CLSID que se implementan en ole32.dll, comadmin.dll, comsvcs.dll o es.dll, o que implementan el \_ identificador de categoría del contador de referencias CATID.

\_El contador de referencias CATID es un GUID de categoría de componente que se puede asociar a un CLSID que se va a serializar. Las interfaces a las que se calculan las referencias personalizadas con este CLSID se permiten cuando EOAC \_ no \_ \_ se establece ningún cálculo de referencias personalizado a través de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Categorías del componente](component-categories.md)
</dt> </dl>

 

 