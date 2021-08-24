---
description: La técnica de programación recomendada para establecer contextos en una aplicación que no está habilitada para lápiz es usar las funciones SetInputScope para asociar el contexto con los campos de la aplicación.
ms.assetid: 95b93804-8079-4b97-b1b0-dfc0138c94e8
title: Establecer el contexto con las API SetInputScope
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0abe9992e4a4ee81190fdee022b11f443592e05d7c99f9a5e69d0a200f63ecbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708155"
---
# <a name="setting-context-with-the-setinputscope-apis"></a>Establecer el contexto con las API SetInputScope

La técnica de programación recomendada para establecer contextos en una aplicación que no está habilitada para lápiz es usar las funciones [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) para asociar el contexto con los campos de la aplicación.

Microsoft Windows XP Tablet PC Edition Development Kit 1.7 fue la primera versión de Microsoft Windows que [**ofrecía SetInputScope.**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) Windows Vista también proporciona compatibilidad con estas funciones. Las **definiciones setInputScope** se declaran en InputScope.idl y InputScope.h. Para obtener más información, [vea Text Services Framework](../tsf/text-services-framework.md).

Las [**funciones SetInputScope son**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) la manera recomendada de establecer el contexto para los controles y las aplicaciones que no tienen habilitada la entrada de lápiz.

## <a name="common-input-scopes"></a>Ámbitos de entrada comunes

Con las [**funciones SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) y el conjunto definido de ámbitos de entrada comunes descritos en la enumeración [**InputScope,**](/windows/win32/api/inputscope/ne-inputscope-inputscope) puede mejorar la precisión del reconocimiento de los reconocedores de escritura a mano de Microsoft.

> [!Note]  
> Los reconocedores de inglés (Estados Unidos), inglés (Reino Unido), alemán, francés, italiano, español, neerlandés y portugués admiten actualmente el uso de los ámbitos de entrada comunes [**con SetInputScope.**](/windows/win32/api/inputscope/nf-inputscope-setinputscope)

 

 

 
