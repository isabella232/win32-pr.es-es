---
description: 'Un proveedor de métodos debe implementar IWbemServices como la interfaz principal. Sin embargo, un proveedor de método puro solo requiere que se implemente el método IWbemServices:: ExecMethodAsync.'
ms.assetid: 39466513-48f3-4bf6-a3ab-e9d2c387480c
ms.tgt_platform: multiple
title: Implementar la interfaz principal para un proveedor de métodos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 196f87a6520d92bf18362be88f8cc40e5133dabe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706757"
---
# <a name="implementing-the-primary-interface-for-a-method-provider"></a>Implementar la interfaz principal para un proveedor de métodos

Un proveedor de métodos debe implementar [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) como la interfaz principal. Sin embargo, un proveedor de método puro solo requiere que se implemente el método [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) .

Dado que otros proveedores usan [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), la interfaz contiene muchos métodos que son irrelevantes para un proveedor de métodos puros. El proveedor de método puro debe proporcionar una implementación de código auxiliar que devuelva el \_ proveedor WBEM E \_ \_ no \_ sea compatible con todos los demás métodos **IWbemServices** además de [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync). Sin embargo, muchos proveedores de métodos también sirven como proveedores de instancias o de clases. Los proveedores de instancias y métodos combinados deben admitir más métodos **IWbemServices** .

 

 



