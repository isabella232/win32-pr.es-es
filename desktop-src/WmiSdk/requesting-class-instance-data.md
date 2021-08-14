---
description: Las consultas de datos son instrucciones WQL que solicitan instancias de clases. Para emitir una consulta de datos, las aplicaciones llaman al método IWbemServices::ExecQuery o IWbemServices::ExecQueryAsync.
ms.assetid: a8b9bf2f-300d-4570-8b30-7532f3421d39
ms.tgt_platform: multiple
title: Solicitud de datos de instancia de clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332ff8b5ba0aae7d1ac33fb8faba6340bbd795401fa81a52ea9c21abc4fde2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316292"
---
# <a name="requesting-class-instance-data"></a>Solicitud de datos de instancia de clase

Las consultas de datos son instrucciones WQL que solicitan instancias de clases. Para emitir una consulta de datos, las aplicaciones llaman al método [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) o [**IWbemServices::ExecQueryAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)

Las instrucciones siguientes se usan para realizar consultas de datos:

-   [SELECT](select-statement-for-data-queries.md)
-   [ASOCIADORES DE](associators-of-statement.md)
-   [REFERENCIAS DE](references-of-statement.md)
-   [ISA](isa-operator-for-data-queries.md)

La instrucción SELECT de WQL es la instrucción Lenguaje de consulta estructurado estándar (SQL) para recuperar información, con algunas restricciones y extensiones específicas de WQL. Aunque la SQL SELECT se usa normalmente en el entorno de base de datos para recuperar columnas concretas de tablas, la instrucción SELECT de WQL se usa en WMI para recuperar instancias de una sola clase. WQL no admite consultas en varias clases.

Las instrucciones ASSOCIATORS OF y REFERENCES OF son específicas de WQL y no forman parte de las instrucciones SQL. La instrucción ASSOCIATORS OF recupera todas las instancias de clase asociadas a una instancia de clase de origen determinada y REFERENCES OF recupera todas las instancias que hacen referencia a una instancia de origen determinada. Las asociaciones se representan mediante instancias de una [clase de asociación](declaring-an-association-class.md).

 

 



