---
description: Un IME implementa una característica denominada &\# 0034;reconversion&\# 0034;.
ms.assetid: 32b20872-7e5c-487e-99bb-9447ac3aebd4
title: Uso de Reconversion con un IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd5a0453b6ac94da805e00639d2a7a56fd79deca4027d23d47e33aab93e4009b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146848"
---
# <a name="using-reconversion-with-an-ime"></a>Uso de Reconversion con un IME

Un IME implementa una característica denominada "reconversión". Normalmente, IMM determina las listas de candidatos solo en función de las entradas que escriba el usuario. La reconversión permite que IMM determine uno o varios candidatos en función de la oración que lo contiene (el contexto). Los tipos de reconversión definidos son simples, normales y mejorados.

La reconversión es útil cuando un usuario observa un error de composición en un documento. El usuario puede seleccionar el error y elegir la reconversión en un menú. El IME usa el contexto para determinar el mejor reemplazo. La aplicación puede usar [**ImmSetCompositionString para**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) admitir la reconversión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Administrador de métodos de entrada](using-input-method-manager.md)
</dt> </dl>

 

 



