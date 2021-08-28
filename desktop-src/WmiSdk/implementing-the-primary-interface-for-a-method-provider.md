---
description: Un proveedor de métodos debe implementar IWbemServices como la interfaz principal. Sin embargo, un proveedor de método puro solo requiere que implemente el método IWbemServices::ExecMethodAsync.
ms.assetid: 39466513-48f3-4bf6-a3ab-e9d2c387480c
ms.tgt_platform: multiple
title: Implementar la interfaz principal para un proveedor de métodos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709fcc698155ad0a9e786636045654b08d1cd2b7dfabd946b2d3ee9e8192485
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244235"
---
# <a name="implementing-the-primary-interface-for-a-method-provider"></a>Implementar la interfaz principal para un proveedor de métodos

Un proveedor de métodos debe [**implementar IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) como la interfaz principal. Sin embargo, un proveedor de método puro solo requiere que implemente el [**método IWbemServices::ExecMethodAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)

Dado que otros proveedores [**usan IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)la interfaz contiene muchos métodos que son irrelevantes para un proveedor de métodos puros. El proveedor de métodos puros debe proporcionar una implementación de código auxiliar que devuelva WBEM E PROVIDER NOT CAPABLE para todos los demás \_ \_ \_ \_ **métodos IWbemServices** además de [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync). Sin embargo, muchos proveedores de métodos también sirven como proveedores de instancias o clases. Los proveedores de instancias y métodos combinados deben admitir más de **los métodos IWbemServices.**

 

 



