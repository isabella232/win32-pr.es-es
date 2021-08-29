---
description: Un objeto incrustado es un objeto de una clase que existe dentro de una declaración de clase o instancia de otra clase.
ms.assetid: 11a4556b-f682-4850-aedc-793602c5745b
ms.tgt_platform: multiple
title: Insertar objetos en una clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bae37a6ce79638af4b508253ae8b61e03abb98e25aea095ab60f685279eefef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679762"
---
# <a name="embedding-objects-in-a-class"></a>Insertar objetos en una clase

Un objeto incrustado es un objeto de una clase que existe dentro de una declaración de clase o instancia de otra clase. Por ejemplo, la [**clase \_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) contiene objetos [**\_ incrustados Win32 Trustee.**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) Cada uno de los **objetos De confianza \_ de Win32** contiene un [**objeto ACE \_ de Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) WMI no limita la profundidad a la que una clase puede tener objetos incrustados. Sin embargo, el uso de otro diseño, como la creación de una clase de asociación, puede crear un esquema más fácil de administrar.

Para obtener más información sobre los objetos incrustados, vea los temas siguientes:

-   [Crear objetos incrustados](creating-embedded-objects.md)
-   [Consulta de objetos incrustados](querying-embedded-objects.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
