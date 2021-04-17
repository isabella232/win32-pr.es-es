---
description: 'Las consultas de datos son instrucciones WQL que solicitan instancias de clases. Para emitir una consulta de datos, las aplicaciones llaman al método IWbemServices:: ExecQuery o IWbemServices:: ExecQueryAsync.'
ms.assetid: a8b9bf2f-300d-4570-8b30-7532f3421d39
ms.tgt_platform: multiple
title: Solicitar datos de instancia de clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32df053ae1267f396978d98271f57f174ea6bf0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697733"
---
# <a name="requesting-class-instance-data"></a>Solicitar datos de instancia de clase

Las consultas de datos son instrucciones WQL que solicitan instancias de clases. Para emitir una consulta de datos, las aplicaciones llaman al método [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) o [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) .

Las instrucciones siguientes se utilizan para realizar consultas de datos:

-   [SELECT](select-statement-for-data-queries.md)
-   [ASSOCIATORS OF](associators-of-statement.md)
-   [REFERENCIAS DE](references-of-statement.md)
-   [ISA](isa-operator-for-data-queries.md)

La instrucción SELECT de WQL es la instrucción de Lenguaje de consulta estructurado estándar (SQL) para recuperar información, con algunas restricciones y extensiones específicas de WQL. Aunque la instrucción SELECT de SQL se usa normalmente en el entorno de base de datos para recuperar columnas concretas de las tablas, la instrucción SELECT de WQL se usa en WMI para recuperar instancias de una sola clase. WQL no admite consultas en varias clases.

Los asociados de y las referencias de las instrucciones son específicos de WQL y no forman parte de SQL estándar. La instrucción ASSOCIATORS OF recupera todas las instancias de clase que están asociadas a una instancia de clase de origen determinada, y las referencias de recuperan todas las instancias que hacen referencia a una instancia de origen determinada. Las asociaciones se representan mediante instancias de una [clase de asociación](declaring-an-association-class.md).

 

 



