---
description: Enumera los valores devueltos por las funciones de administración de seguridad.
ms.assetid: ee55364e-8ffe-4a78-a49a-250756561770
title: Valores devueltos de administración de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd2c67b79d03896960f7eb9a8631e1cd268284e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688248"
---
# <a name="security-management-return-values"></a>Valores devueltos de administración de seguridad

Los valores devueltos de administración de seguridad incluyen los siguientes:

-   [Valores devueltos adjuntos](#attachment-return-values)
-   [Valores devueltos de la función de directiva LSA](#lsa-policy-function-return-values)

## <a name="attachment-return-values"></a>Valores devueltos adjuntos

El conjunto de herramientas de configuración de seguridad admite los siguientes códigos de retorno de **SCESTATUS** . Estos valores son devueltos por las funciones de soporte de datos adjuntos y las funciones implementadas al escribir un motor de datos adjuntos o un complemento.



| Value                            | Descripción                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------|
| SCESTATUS \_ correcto               | La función se ha realizado correctamente.                                                                          |
| SCESTATUS \_ parámetro no válido \_    | Uno de los parámetros pasados a la función no era válido.                                      |
| \_ \_ no \_ se encontró el registro SCESTATUS    | No se encontró el registro especificado en la base de datos de seguridad.                                     |
| SCESTATUS \_ datos no válidos \_         | Error de la función porque algunos datos no eran válidos.                                             |
| \_existe el objeto SCESTATUS \_        | El objeto ya existe.                                                                       |
| búfer de SCESTATUS \_ \_ demasiado \_ pequeño    | El búfer que se pasa a la función para recibir datos no es lo suficientemente grande como para recibir todos los datos. |
| \_ \_ no \_ se encontró el perfil SCESTATUS   | No se encontró el perfil especificado.                                                             |
| SCESTATUS \_ \_ formato incorrecto           | El formato no es válido.                                                                         |
| \_no \_ hay \_ recursos suficientes para SCESTATUS | Memoria insuficiente.                                                                    |
| SCESTATUS \_ acceso \_ denegado        | El autor de la llamada no tiene privilegios suficientes para completar esta acción.                          |
| SCESTATUS no se pudo \_ \_ eliminar          | La función no puede eliminar el elemento especificado.                                                   |
| \_desbordamiento de prefijo SCESTATUS \_      | Se produjo un desbordamiento de prefijo.                                                                      |
| SCESTATUS \_ otro \_ error          | Error no especificado.                                                               |
| SCESTATUS \_ ya se está \_ ejecutando      | El servicio ya se está ejecutando.                                                                  |
| el \_ servicio SCESTATUS \_ no es \_ compatible | No se admite el servicio especificado.                                                          |
| SCESTATUS \_ mod \_ no \_ encontrado       | No se puede encontrar o cargar una DLL del motor de datos adjuntos en el registro.      |
| \_excepción \_ de SCESTATUS en el \_ servidor | Se produjo una excepción en el servidor.                                                             |



 

## <a name="lsa-policy-function-return-values"></a>Valores devueltos de la función de directiva LSA

La mayoría de las funciones de directiva de [*autoridad de seguridad local*](/windows/desktop/SecGloss/l-gly) (LSA) devuelven un valor de NTSTATUS para indicar si se ha realizado correctamente o no. Los distintos valores de NTSTATUS se definen en NTSTATUS. h, que se distribuye con el kit de desarrollo de controladores (DDK) de Microsoft Windows.

Para convertir un valor de devolución de NTSTATUS en un código de error de Windows, utilice la función [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) .

En la tabla siguiente se enumeran los valores de NTSTATUS que podrían ser devueltos por cualquier función de LSA. (Las secciones de valores devueltos de algunas de las funciones de LSA muestran códigos de error adicionales que la función puede devolver). En esta tabla también se muestra el código de error de Windows que corresponde a cada valor de NTSTATUS.



| Código NTSTATUS (código de error de Windows)                                        | Significado                                                                                                                                 |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| ESTADO \_ correcto (error \_ correcto)<br/>                               | La función se realizó correctamente.                                                                                                            |
| ESTADO \_ acceso \_ denegado (error de \_ acceso \_ denegado)<br/>                 | El autor de la llamada no tiene el acceso adecuado para completar la operación.                                                                  |
| Estado de \_ recursos insuficientes \_ (error \_ sin \_ recursos del sistema \_ )<br/> | No hay suficientes recursos del sistema (como la memoria para asignar búferes) para completar la llamada.                                        |
| ESTADO \_ error interno de la \_ base de BD (error interno de la \_ base de \_ \_ BD \_ )<br/>       | La base de datos LSA contiene una incoherencia interna.                                                                                    |
| ESTADO \_ de \_ identificador no válido (error de \_ identificador no válido \_ )<br/>               | Indica que un objeto o un identificador de RPC no es válido en el [*contexto*](/windows/desktop/SecGloss/c-gly) utilizado.     |
| estado \_ estado \_ del servidor no válido \_ (error de \_ Estado de servidor no válido \_ \_ )<br/> | Indica que el servidor LSA está deshabilitado actualmente.                                                                                         |
| ESTADO \_ parámetro no válido \_ (error de \_ parámetro no válido \_ )<br/>         | Uno de los parámetros no es válido.                                                                                                     |
| \_no tiene \_ este \_ privilegio de estado ( \_ no hay ningún \_ privilegio de este tipo \_ )<br/>       | Indica que un privilegio especificado no existe.                                                                                         |
| \_ \_ no se encontró el nombre de objeto de estado \_ \_ (archivo de error \_ \_ no \_ encontrado)<br/>     | No se encontró un objeto en la base de datos de directivas de LSA. Es posible que el objeto se haya especificado por SID o por nombre, en función de su tipo. |
| ESTADO \_ incorrecto (error de generación de error \_ \_ )<br/>                     | Error genérico, como un error de conexión RPC.                                                                                        |



 

 

