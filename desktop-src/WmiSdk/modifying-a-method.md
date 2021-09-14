---
description: Además de clases e instancias, WMI permite modificar un método. La razón principal por la que desea modificar un método es si cambia la implementación de un método en un proveedor. Para obtener más información, vea Escribir un proveedor de métodos.
ms.assetid: 239a994f-ecaf-4558-9626-8f5e60dd350c
ms.tgt_platform: multiple
title: Modificar un método
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93009891deec8651599f73f14a73f83bba8ffd4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973759"
---
# <a name="modifying-a-method"></a>Modificar un método

Además de clases e instancias, WMI permite modificar un método. La razón principal por la que desea modificar un método es si cambia la implementación de un método en un proveedor. Para obtener más información, vea [Escribir un proveedor de métodos](writing-a-method-provider.md).

La modificación de un método no es una operación que se pueda realizar en el script.

En el procedimiento siguiente se describe cómo modificar un método mediante programación.

**Para modificar un método mediante programación**

1.  Recupere la definición de clase con una llamada a [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod).

    Los dos parámetros out, *ppInSignature* y *ppOutSignature,* contienen la clase in-parameter y la clase out-parameter, respectivamente. El valor devuelto se agrupa en la clase out-parameter como una propiedad y debe denominarse **ReturnValue.**

2.  Recupere y modifique los parámetros con llamadas a [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**IWbemClassObject::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)o [**IWbemClassObject::D elete**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete).
3.  Vuelva a colocar la nueva versión del método en la clase primaria con una llamada a [**IWbemClassObject::P utMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

Para obtener más información, vea [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).

 

 



