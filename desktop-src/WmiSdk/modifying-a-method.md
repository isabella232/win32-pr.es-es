---
description: Además de las clases e instancias, WMI permite modificar un método. La razón principal por la que desea modificar un método es si ha cambiado la implementación de un método en un proveedor. Para obtener más información, consulte escribir un proveedor de métodos.
ms.assetid: 239a994f-ecaf-4558-9626-8f5e60dd350c
ms.tgt_platform: multiple
title: Modificar un método
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93009891deec8651599f73f14a73f83bba8ffd4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423596"
---
# <a name="modifying-a-method"></a>Modificar un método

Además de las clases e instancias, WMI permite modificar un método. La razón principal por la que desea modificar un método es si ha cambiado la implementación de un método en un proveedor. Para obtener más información, consulte [escribir un proveedor de métodos](writing-a-method-provider.md).

Modificar un método no es una operación que se puede realizar en el script.

En el procedimiento siguiente se describe cómo modificar un método mediante programación.

**Para modificar un método mediante programación**

1.  Recupere la definición de clase con una llamada a [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod).

    Los dos parámetros out, *ppInSignature* y *ppOutSignature*, contienen la clase in-parameter y la clase out-Parameter, respectivamente. El valor devuelto se incluye en la clase out-Parameter como una propiedad y se debe denominar **ReturnValue**.

2.  Recupere y modifique los parámetros con llamadas a [**IWbemClassObject:: get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)o [**IWbemClassObject::D iminar**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete).
3.  Vuelva a colocar la nueva versión del método en la clase primaria con una llamada a [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

Para obtener más información, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md).

 

 



