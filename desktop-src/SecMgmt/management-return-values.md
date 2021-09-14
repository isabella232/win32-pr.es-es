---
description: Enumera los valores devueltos por las funciones de administración de seguridad.
ms.assetid: ee55364e-8ffe-4a78-a49a-250756561770
title: Valores devueltos de administración de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd2c67b79d03896960f7eb9a8631e1cd268284e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243999"
---
# <a name="security-management-return-values"></a>Valores devueltos de administración de seguridad

Los valores devueltos de administración de seguridad incluyen los siguientes:

-   [Valores devueltos de datos adjuntos](#attachment-return-values)
-   [Valores devueltos de la función de directiva LSA](#lsa-policy-function-return-values)

## <a name="attachment-return-values"></a>Valores devueltos de datos adjuntos

El conjunto de herramientas configuración de seguridad admite los siguientes códigos **de retorno SCESTATUS.** Estos valores los devuelven las funciones de compatibilidad de datos adjuntos y las funciones implementadas al escribir un motor de datos adjuntos o un complemento.



| Value                            | Descripción                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------|
| SCESTATUS \_ SUCCESS               | La función se ha realizado correctamente.                                                                          |
| PARÁMETRO SCESTATUS \_ INVALID \_    | Uno de los parámetros pasados a la función no era válido.                                      |
| REGISTRO SCESTATUS \_ \_ NO \_ ENCONTRADO    | No se encontró el registro especificado en la base de datos de seguridad.                                     |
| DATOS NO \_ VÁLIDOS DE SCESTATUS \_         | Error en la función porque algunos datos no son válidos.                                             |
| EXISTE EL OBJETO SCESTATUS \_ \_        | El objeto ya existe.                                                                       |
| BÚFER SCESTATUS \_ \_ DEMASIADO \_ PEQUEÑO    | El búfer pasado a la función para recibir datos no es lo suficientemente grande como para recibir todos los datos. |
| PERFIL DE SCESTATUS \_ \_ NO \_ ENCONTRADO   | No se encontró el perfil especificado.                                                             |
| FORMATO NO CORRECTO DE SCESTATUS \_ \_           | El formato no es válido.                                                                         |
| SCESTATUS \_ NO ES SUFICIENTE \_ \_ RECURSO | No hay memoria suficiente.                                                                    |
| ACCESO DENEGADO DE SCESTATUS \_ \_        | El autor de la llamada no tiene privilegios suficientes para completar esta acción.                          |
| SCESTATUS \_ CANT \_ DELETE          | La función no puede eliminar el elemento especificado.                                                   |
| DESBORDAMIENTO DE PREFIJO SCESTATUS \_ \_      | Se produjo un desbordamiento de prefijo.                                                                      |
| SCESTATUS \_ OTHER \_ ERROR          | Error no especificado.                                                               |
| SCESTATUS \_ YA EN \_ EJECUCIÓN      | El servicio ya se está ejecutando.                                                                  |
| NO SE ADMITE EL SERVICIO SCESTATUS \_ \_ \_ | No se admite el servicio especificado.                                                          |
| SCESTATUS \_ MOD \_ NO \_ ENCONTRADO       | No se encuentra un archivo DLL del motor de datos adjuntos que aparece en el registro o no se puede cargar.      |
| EXCEPCIÓN SCESTATUS \_ \_ EN EL \_ SERVIDOR | Se produjo una excepción en el servidor.                                                             |



 

## <a name="lsa-policy-function-return-values"></a>Valores devueltos de la función de directiva LSA

La [*mayoría de las funciones*](/windows/desktop/SecGloss/l-gly) de directiva de autoridad de seguridad local (LSA) devuelven un valor NTSTATUS para indicar que la operación se ha hecho correctamente o no. Los distintos valores NTSTATUS se definen en Ntstatus.h, que se distribuye con microsoft Windows Driver Development Kit (DDK).

Para convertir un valor devuelto NTSTATUS en un Windows de error, use la función [**LsaNtStatusToWinError.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror)

En la tabla siguiente se enumeran los valores NTSTATUS que puede devolver cualquier función LSA. (Las secciones de valor devuelto de algunas de las funciones LSA enumeran códigos de error adicionales que la función podría devolver). En esta tabla también se muestra Windows código de error que corresponde a cada valor NTSTATUS.



| Código NTSTATUS (Windows de error)                                        | Significado                                                                                                                                 |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| ESTADO \_ CORRECTO (ERROR \_ CORRECTO)<br/>                               | La función se ha realizado correctamente.                                                                                                            |
| ACCESO DE \_ ESTADO \_ DENEGADO (ACCESO DE ERROR \_ \_ DENEGADO)<br/>                 | El autor de la llamada no tiene el acceso adecuado para completar la operación.                                                                  |
| RECURSOS \_ \_ INSUFICIENTES DE ESTADO (ERROR \_ SIN RECURSOS DEL \_ \_ SISTEMA)<br/> | No hay suficientes recursos del sistema (como memoria para asignar búferes) para completar la llamada.                                        |
| ERROR DE BASE DE DATOS INTERNA DE ESTADO \_ \_ \_ (ERROR \_ INTERNO DE BASE \_ DE \_ DATOS)<br/>       | La base de datos LSA contiene una incoherencia interna.                                                                                    |
| IDENTIFICADOR \_ DE ESTADO NO VÁLIDO \_ (IDENTIFICADOR NO VÁLIDO DE \_ \_ ERROR)<br/>               | Indica que un objeto o identificador RPC no es válido en el [*contexto utilizado.*](/windows/desktop/SecGloss/c-gly)     |
| ESTADO \_ ESTADO DE SERVIDOR NO VÁLIDO \_ \_ (ERROR ESTADO DE SERVIDOR NO \_ \_ \_ VÁLIDO)<br/> | Indica que el servidor LSA está deshabilitado actualmente.                                                                                         |
| PARÁMETRO \_ STATUS INVALID \_ (ERROR INVALID \_ \_ PARAMETER)<br/>         | Uno de los parámetros no es válido.                                                                                                     |
| STATUS \_ NO \_ SUCH \_ PRIVILEGE (ERROR \_ NO \_ SUCH \_ PRIVILEGE)<br/>       | Indica que no existe un privilegio especificado.                                                                                         |
| NO \_ SE ENCONTRÓ EL NOMBRE DEL OBJETO DE ESTADO \_ \_ \_ (NO SE ENCONTRÓ EL ARCHIVO DE \_ \_ \_ ERROR)<br/>     | No se encontró un objeto en la base de datos de directivas LSA. El objeto se puede haber especificado por SID o por nombre, dependiendo de su tipo. |
| ESTADO \_ NO CORRECTO (ERROR DE \_ \_ GENERACIÓN DE ERRORES)<br/>                     | Error genérico, como un error de conexión RPC.                                                                                        |



 

 

