---
description: En el ejemplo de código siguiente se muestra la creación del objeto TAPI.
ms.assetid: f8566e53-51c9-4424-a8bb-369455f35706
title: Inicializar TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78062e71df2d68895a645ca8a6c4c480a1415cd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912777"
---
# <a name="initialize-tapi"></a>Inicializar TAPI

En el ejemplo de código siguiente se muestra la creación del objeto TAPI.

```cpp
const auto result = ITTAPI::Initialize();

if (result != S_OK) {
    switch (result) {
        case S_FALSE: {
            std::cerr << "TAPI has already been initialized.\n";
        } break;

        [[fallthrough]]
        case E_OUTOFMEMORY: {
            std::cerr << "Insufficient memory exists to perform the operation.\n";
        }

        default: {
            // TODO: Handle unrecoverable error here
        }
    }
}
```

## <a name="see-also"></a>Consulte también

- [ITTAPI:: Initialize](/windows/win32/api/tapi3if/nf-tapi3if-ittapi-initialize)
- [Valores HRESULT comunes](../seccrypto/common-hresult-values.md)
