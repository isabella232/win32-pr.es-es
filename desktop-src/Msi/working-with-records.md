---
description: El instalador proporciona funciones que manipulan los registros de una base de datos de instalación. Estas funciones se pueden usar junto con las funciones descritas en Trabajar con consultas para realizar cambios reales en una base de datos.
ms.assetid: 5ea3fb1d-ddcb-4013-84dc-dd6f90c5751a
title: Trabajar con registros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3252dc29bf755d08494dbdc2326bf45a4afb1c91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071805"
---
# <a name="working-with-records"></a>Trabajar con registros

El instalador proporciona funciones que manipulan los registros de una base de datos de instalación. Estas funciones se pueden usar junto con las funciones descritas en [Trabajar](working-with-queries.md) con consultas para realizar cambios reales en una base de datos.

Las siguientes funciones crean o quitan registros:

-   Para crear un nuevo registro para una base de datos, llame a la [**función MsiCreateRecord.**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord)
-   Para borrar datos de un registro, establezca cada campo en NULL mediante una llamada a la [**función MsiRecordClearData.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata)

Las siguientes funciones rellenan los campos de registros especificados:

-   Para establecer un registro en un entero, llame a la [**función MsiRecordSetInteger.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)
-   Para establecer un registro en una cadena, llame a la [**función MsiRecordSetString.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa)
-   Para insertar un archivo completo en un campo de secuencia, llame a la [**función MsiRecordSetStream.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama)

Las siguientes funciones leen valores de campos de registros especificados:

-   Para leer un valor entero de un campo, llame a la [**función MsiRecordGetInteger.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger)
-   Para recuperar un valor de cadena, llame a [**la función MsiRecordGetString.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)
-   Para obtener una secuencia, llame a [**la función MsiRecordReadStream.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream)
-   Para determinar si un campo determinado de un registro es NULL, llame a la [**función MsiRecordIsNull.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull)

Las siguientes funciones son funciones de registro informativo:

-   Para obtener el número de campos que contiene un registro, llame a la [**función MsiRecordGetFieldCount.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount)
-   Para obtener el tamaño de un campo, llame a la [**función MsiRecordDataSize.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) El valor devuelto de **MsiRecordDataSize** es sensible al tipo de campo.

 

 



