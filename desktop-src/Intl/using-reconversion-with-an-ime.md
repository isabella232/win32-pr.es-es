---
description: Un IME implementa una característica llamada &\# 0034; reconversión&\# 0034;.
ms.assetid: 32b20872-7e5c-487e-99bb-9447ac3aebd4
title: Usar la reconversión con un IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e28383a27fd7fd7827cbbf3c7ff97c895fb4a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677262"
---
# <a name="using-reconversion-with-an-ime"></a>Usar la reconversión con un IME

Un IME implementa una característica denominada "reconversión". Normalmente, el IMM determina las listas de candidatos basándose solo en las entradas escritas por el usuario. La reconversión permite al IMM determinar uno o más candidatos en función de la oración que lo contiene (el contexto). Los tipos de conversión definidos son simple, normal y mejorado.

La reconversión resulta útil cuando un usuario observa un error de composición en un documento. El usuario puede seleccionar el error y elegir reconversión en un menú. El IME usa el contexto para determinar el mejor reemplazo. La aplicación puede utilizar [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) para admitir la reconversión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el administrador de métodos de entrada](using-input-method-manager.md)
</dt> </dl>

 

 



