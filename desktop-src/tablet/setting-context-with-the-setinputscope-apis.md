---
description: La técnica de programación recomendada para establecer contextos en una aplicación que no está habilitada para tinta es usar las funciones de SetInputScope para asociar el contexto con los campos de la aplicación.
ms.assetid: 95b93804-8079-4b97-b1b0-dfc0138c94e8
title: Configuración del contexto con las API de SetInputScope
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c1b507b1719bea8c04288dca9214ad5675f8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678039"
---
# <a name="setting-context-with-the-setinputscope-apis"></a>Configuración del contexto con las API de SetInputScope

La técnica de programación recomendada para establecer contextos en una aplicación que no está habilitada para tinta es usar las funciones de [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) para asociar el contexto con los campos de la aplicación.

El kit de desarrollo de Microsoft Windows XP Tablet PC Edition 1,7 era la primera versión de Microsoft Windows para ofrecer [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope). Windows Vista también proporciona compatibilidad con estas funciones. Las definiciones de **SetInputScope** se declaran en InputScope. idl e InputScope. h. Para obtener más información, vea [Text Services Framework](../tsf/text-services-framework.md).

Las funciones [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) son el método recomendado para establecer el contexto de los controles y las aplicaciones que no están habilitadas para tinta.

## <a name="common-input-scopes"></a>Ámbitos de entrada comunes

Con las funciones [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) y el conjunto definido de ámbitos de entrada comunes descritos en la enumeración [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) , puede mejorar la precisión del reconocimiento de los reconocedores de escritura a mano de Microsoft.

> [!Note]  
> Los reconocedores para inglés (Estados Unidos), Inglés (Reino Unido), alemán, Francés, Italiano, español, holandés y Portugués actualmente admiten el uso de los ámbitos de entrada comunes con [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).

 

 

 
