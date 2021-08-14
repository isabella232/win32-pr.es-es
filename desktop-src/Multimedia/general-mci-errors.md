---
title: Errores generales de MCI
description: Errores generales de MCI
ms.assetid: be9c4a2b-44bc-410c-be74-ba55bb4e785b
keywords:
- Valores devueltos de MCIERR, errores generales
- referencia multimedia, errores de MCI
- referencia de multimedia, errores de MCI
- Interfaz de control multimedia (MCI), errores generales
- MCI (interfaz de control multimedia), errores generales
- referencia de MCI, errores generales
- Referencia de MCI, errores generales
- Interfaz de control multimedia (MCI), errores
- MCI (interfaz de control multimedia), errores
- referencia de MCI, errores
- Referencia de MCI, errores
- Función mciSendCommand
- Función mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6f402e532f1bcf22a9136764647c91b1f4d54479f932c509ec172c1d973f4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375162"
---
# <a name="general-mci-errors"></a>Errores generales de MCI

La función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) o [**mciSendString**](/previous-versions//dd757161(v=vs.85)) pueden devolver los siguientes valores de error:



| Valor                            | Significado                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FORMATO DE HORA \_ DE MCIERR \_ \_        | El valor especificado para el formato de hora no es válido.                                                                                                         |
| MCIERR \_ NO PUEDE CARGAR EL \_ \_ CONTROLADOR     | El controlador de dispositivo especificado no se cargará correctamente.                                                                                                         |
| MCIERR \_ NO PUEDE USAR \_ \_ ALL         | No se permite el nombre de dispositivo "all" para este comando.                                                                                                      |
| MCIERR \_ CREATEWINDOW             | No se pudo crear ni usar la ventana.                                                                                                                             |
| LONGITUD DEL DISPOSITIVO MCIERR \_ \_           | El nombre del dispositivo o del controlador es demasiado largo. Especifique un nombre de dispositivo o controlador con menos de 79 caracteres.                                                     |
| DISPOSITIVO MCIERR \_ \_ BLOQUEADO           | El dispositivo se está cierrando. Espere unos segundos e inténtelo de nuevo.                                                                                         |
| DISPOSITIVO MCIERR \_ \_ NO \_ INSTALADO   | El dispositivo especificado no está instalado en el sistema. Use la opción Controladores del Panel de control para instalar el dispositivo.                                   |
| DISPOSITIVO MCIERR \_ \_ NO \_ LISTO       | El controlador del dispositivo no está listo.                                                                                                                             |
| DISPOSITIVO MCIERR \_ \_ ABIERTO             | Esta aplicación ya usa el nombre del dispositivo como alias. Use un alias único.                                                                        |
| LONGITUD DEL \_ \_ ORD DEL DISPOSITIVO MCIERR \_      | El nombre del dispositivo o del controlador es demasiado largo. Especifique un nombre de dispositivo o controlador con menos de 79 caracteres.                                                     |
| SE REQUIERE EL \_ TIPO \_ DE DISPOSITIVO \_ MCIERR   | No se encuentra el dispositivo especificado en el sistema. Compruebe que el dispositivo está instalado y que el nombre del dispositivo está escrito correctamente.                            |
| CONTROLADOR \_ MCIERR                   | El controlador del dispositivo presenta un problema. Consulte con el fabricante del dispositivo para obtener un nuevo controlador.                                                      |
| MCIERR \_ DRIVER \_ INTERNAL         | El controlador del dispositivo presenta un problema. Consulte con el fabricante del dispositivo para obtener un nuevo controlador.                                                      |
| ALIAS DUPLICADO DE MCIERR \_ \_         | El alias especificado ya se usa en esta aplicación. Use un alias único.                                                                                |
| NO SE ENCONTRÓ LA EXTENSIÓN MCIERR \_ \_ \_    | La extensión especificada no tiene ningún tipo de dispositivo asociado. Especifique un tipo de dispositivo.                                                                       |
| CARACTERES \_ ADICIONALES DE MCIERR \_        | Debe incluir una cadena entre comillas; Los caracteres que aparecen después de la comilla de cierre no son válidos.                                              |
| ARCHIVO MCIERR \_ \_ NO \_ ENCONTRADO         | No se encontró el archivo solicitado. Compruebe que la ruta de acceso y el nombre de archivo son correctos.                                                                             |
| ARCHIVO MCIERR \_ \_ NO \_ GUARDADO         | El archivo no se guardó. Asegúrese de que el sistema tiene suficiente espacio en disco o de que tiene una conexión de red intacta.                                                |
| MCIERR \_ FILE \_ READ               | Error al leer el archivo. Asegúrese de que el archivo está presente en el sistema o de que el sistema tiene una conexión de red intacta.                             |
| ESCRITURA DE \_ ARCHIVOS MCIERR \_              | Error al escribir en el archivo. Asegúrese de que el sistema tiene suficiente espacio en disco o de que tiene una conexión de red intacta.                                            |
| SE REQUIERE NOMBRE \_ DE ARCHIVO MCIERR \_       | El nombre de archivo no es válido. Asegúrese de que el nombre de archivo no tiene más de ocho caracteres, seguido de un punto y una extensión.                                  |
| MARCAS MCIERR \_ \_ NO \_ COMPATIBLES   | Los parámetros especificados no se pueden usar juntos.                                                                                                           |
| MCIERR \_ GET \_ CD                  | No se encontró el archivo solicitado o el dispositivo MCI. Intente cambiar directorios o reiniciar el sistema.                                                         |
| HARDWARE DE MCIERR \_                 | El dispositivo especificado presenta un problema. Compruebe que el dispositivo funciona correctamente o póngase en contacto con el fabricante del dispositivo.                                     |
| MCIERR \_ ILLEGAL \_ FOR \_ AUTO \_ OPEN | MCI no realizará el comando especificado en un dispositivo abierto automáticamente. Espere hasta que se cierre el dispositivo y, a continuación, intente realizar el comando.             |
| MCIERR \_ INTERNAL                 | Se produjo un problema al inicializar MCI. Intente reiniciar el Windows operativo.                                                                        |
| IDENTIFICADOR DE DISPOSITIVO \_ NO VÁLIDO \_ DE MCIERR \_      | Identificador de dispositivo no válido. Use el identificador que se le dio al dispositivo cuando se abrió el dispositivo.                                                                               |
| NOMBRE DE DISPOSITIVO \_ NO VÁLIDO \_ DE MCIERR \_    | MCI no abre ni reconoce el dispositivo especificado.                                                                                                     |
| ARCHIVO MCIERR \_ NO \_ VÁLIDO            | El archivo especificado no se puede reproducir en el dispositivo MCI especificado. El archivo puede estar dañado o puede usar un formato de archivo incorrecto.                               |
| FALTA EL PARÁMETRO MCIERR \_ \_       | El comando especificado requiere un parámetro , que debe proporcionar.                                                                                          |
| MCIERR \_ MULTIPLE                 | Se produjeron errores en más de un dispositivo. Especifique cada comando y dispositivo por separado para identificar los dispositivos que provocan los errores.                             |
| MCIERR \_ DEBE \_ USAR \_ SHAREABLE     | El controlador del dispositivo ya está en uso. Debe especificar el parámetro "compartible" con cada comando abierto para compartir el dispositivo.                                  |
| MCIERR \_ NO SE PERMITE NINGÚN \_ \_ ELEMENTO     | El dispositivo especificado no usa un nombre de archivo.                                                                                                               |
| MCIERR \_ NO \_ INTEGER              | El parámetro para este comando MCI debe ser un valor entero.                                                                                                |
| MCIERR \_ NO \_ WINDOW               | No hay ninguna ventana para mostrar.                                                                                                                                 |
| FUNCIÓN NO APLICABLE DE \_ MCIERR \_  | La secuencia de comandos de MCI especificada no se puede realizar en el orden especificado. Corrija la secuencia de comandos; a continuación, inténtelo de nuevo.                                   |
| BLOQUE DE PARÁMETROS NULL DE MCIERR \_ \_ \_   | Se pasó un bloque de parámetros NULL (estructura) a MCI.                                                                                                       |
| MEMORIA DE \_ MCIERR \_ \_          | El sistema no tiene suficiente memoria para esta tarea. Salga de una o varias aplicaciones para aumentar la memoria disponible y, a continuación, intente realizar la tarea de nuevo. |
| MCIERR \_ OUTOFRANGE               | El valor de parámetro especificado está fuera del intervalo para el comando MCI especificado.                                                                                |
| MCIERR \_ SET \_ CD                  | No se puede acceder al archivo o dispositivo MCI especificado porque la aplicación no puede cambiar los directorios.                                                         |
| UNIDAD MCIERR \_ \_ SET               | No se puede acceder al archivo o dispositivo MCI especificado porque la aplicación no puede cambiar las unidades.                                                              |
| RECURSO SIN \_ NOMBRE DE MCIERR \_        | No se puede almacenar un archivo sin nombre. Especifique un nombre de archivo.                                                                                                       |
| COMANDO MCIERR \_ NO \_ RECONOCIDO    | El controlador no puede reconocer el comando especificado.                                                                                                          |
| FUNCIÓN NO ADMITIDA \_ DE MCIERR \_    | El controlador de dispositivo MCI que usa el sistema no admite el comando especificado.                                                                           |



 

 

 