---
description: El operador LIKE determina si una cadena de caracteres coincide con un patrón especificado.
ms.assetid: 6cafe696-891d-4b17-8802-4b872f76fc78
ms.tgt_platform: multiple
title: LIKE (operador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9091f44dd131d5d2c30d2d46aa4fc109dcdf02b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696922"
---
# <a name="like-operator"></a>LIKE (operador)

El operador LIKE determina si una cadena de caracteres coincide con un patrón especificado. El patrón especificado puede contener exactamente los caracteres que deben coincidir, o puede contener metacaracteres. En efecto, el operador LIKE busca coincidencias con subcadenas mediante los caracteres comodín de la tabla siguiente.



| Carácter       | Descripción                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[ \]           | Cualquier carácter del intervalo especificado ( \[ a-f \] ) o del conjunto ( \[ abcdef \] ).                                                                                                                 |
| ^               | Cualquier carácter que no esté dentro del intervalo ( \[ ^ a-f \] ) o establecido ( \[ ^ abcdef \] ).                                                                                                                     |
| %               | Cualquier cadena de 0 (cero) o más caracteres. En el ejemplo siguiente se buscan todas las instancias donde "Win" se encuentra en cualquier parte del nombre de clase: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"` |
| \_ (subrayado) | Cualquier carácter. Cualquier carácter de subrayado literal usado en la cadena de consulta debe colocarse entre comillas \[ \] (entre corchetes).                                                             |



 

Por ejemplo, el siguiente código de Power Shell recupera todas las instancias de la clase **Win32 \_ OperatingSystem** cuya propiedad **Name** comienza con **FirstName**:

`Get-WmiObject win32_computerSystem -filter "Name LIKE 'FirstName%'"`

Dado que el carácter de subrayado es un carácter meta, si el destino de la consulta tiene un carácter de subrayado, los \[ \] caracteres de escape "" deben encerrarlo. Por ejemplo, puede consultar todas las clases que tienen un carácter de subrayado doble en el nombre.

Para buscar todas las clases con un subrayado doble en el nombre, debe escapar ambos caracteres de subrayado \[ \] (corchetes), por ejemplo:

`SELECT * FROM meta_class WHERE __CLASS LIKE "%[_][_]%"`

Puede negar una instrucción LIKE mediante NOT; para ello, asegúrese de colocar no directamente delante del nombre del campo. Por ejemplo:

`  Get-WmiObject -computerName "." -query 'Select * FROM Win32_Printer WHERE Local="TRUE"      AND Network ="False" AND DriverName LIKE "%HP%"      AND NOT PortName LIKE "%10.%" AND NOT PortName LIKE "%\\%"'`

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Operadores WQL](wql-operators.md)
</dt> </dl>

 

 



