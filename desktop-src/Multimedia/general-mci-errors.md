---
title: Errores generales de MCI
description: Errores generales de MCI
ms.assetid: be9c4a2b-44bc-410c-be74-ba55bb4e785b
keywords:
- Valores devueltos de MCIERR, errores generales
- referencia multimedia, errores de MCI
- referencia de multimedia, errores de MCI
- Media control Interface (MCI), errores generales
- MCI (media control Interface), errores generales
- referencia de MCI, errores generales
- Referencia de MCI, errores generales
- Media control Interface (MCI), errores
- MCI (interfaz de control multimedia), errores
- referencia de MCI, errores
- Referencia de MCI, errores
- mciSendCommand función)
- mciSendString función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44538937be73c2ccfb1d30de1f1a1c729cc05095
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358858"
---
# <a name="general-mci-errors"></a>Errores generales de MCI

Los siguientes valores de error pueden ser devueltos por la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) o [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :



| Value                            | Significado                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCIERR \_ \_ formato de hora incorrecta \_        | El valor especificado para el formato de hora no es válido.                                                                                                         |
| MCIERR \_ no puede \_ cargar el \_ controlador     | El controlador de dispositivo especificado no se cargará correctamente.                                                                                                         |
| MCIERR \_ no puede \_ usar \_ All         | No se permite el nombre de dispositivo "All" para este comando.                                                                                                      |
| MCIERR \_ CREATEWINDOW             | No se pudo crear o usar la ventana.                                                                                                                             |
| \_longitud del dispositivo MCIERR \_           | El nombre del dispositivo o del controlador es demasiado largo. Especifique un nombre de dispositivo o de controlador que tenga menos de 79 caracteres.                                                     |
| \_dispositivo MCIERR \_ bloqueado           | El dispositivo se está cerrando. Espere unos segundos y vuelva a intentarlo.                                                                                         |
| \_dispositivo MCIERR \_ no \_ instalado   | El dispositivo especificado no está instalado en el sistema. Use la opción controladores del panel de control para instalar el dispositivo.                                   |
| \_dispositivo MCIERR \_ no \_ listo       | El controlador de dispositivo no está listo.                                                                                                                             |
| \_dispositivo MCIERR \_ abierto             | Esta aplicación ya usa el nombre del dispositivo como alias. Use un alias único.                                                                        |
| \_longitud de \_ Ord del dispositivo MCIERR \_      | El nombre del dispositivo o del controlador es demasiado largo. Especifique un nombre de dispositivo o de controlador que tenga menos de 79 caracteres.                                                     |
| se \_ \_ requiere un tipo de dispositivo MCIERR \_   | No se encuentra el dispositivo especificado en el sistema. Compruebe que el dispositivo está instalado y que el nombre del dispositivo está escrito correctamente.                            |
| \_controlador MCIERR                   | El controlador del dispositivo presenta un problema. Consulte al fabricante del dispositivo para obtener un nuevo controlador.                                                      |
| \_controlador MCIERR \_ interno         | El controlador del dispositivo presenta un problema. Consulte al fabricante del dispositivo para obtener un nuevo controlador.                                                      |
| MCIERR \_ alias duplicado \_         | El alias especificado ya se usa en esta aplicación. Use un alias único.                                                                                |
| \_ \_ no \_ se encontró la extensión MCIERR    | La extensión especificada no tiene ningún tipo de dispositivo asociado. Especifique un tipo de dispositivo.                                                                       |
| MCIERR \_ de \_ caracteres adicionales        | Debe incluir una cadena entre comillas; los caracteres que siguen a la comilla de cierre no son válidos.                                              |
| \_ \_ no \_ se encontró el archivo MCIERR         | No se encontró el archivo solicitado. Compruebe que la ruta de acceso y el nombre de archivo son correctos.                                                                             |
| \_no se \_ \_ GUARDÓ el archivo MCIERR         | No se guardó el archivo. Asegúrese de que el sistema tiene suficiente espacio en disco o que tiene una conexión de red intacta.                                                |
| MCIERR \_ lectura de archivo \_               | Error de lectura del archivo. Asegúrese de que el archivo está presente en el sistema o que el sistema tiene una conexión de red intacta.                             |
| \_escritura de archivo MCIERR \_              | Error al escribir en el archivo. Asegúrese de que el sistema tiene suficiente espacio en disco o que tiene una conexión de red intacta.                                            |
| MCIERR \_ filename \_ requerido       | El nombre de archivo no es válido. Asegúrese de que el nombre de archivo no tenga más de ocho caracteres, seguido de un punto y una extensión.                                  |
| \_marcas MCIERR \_ no \_ compatibles   | Los parámetros especificados no se pueden usar juntos.                                                                                                           |
| MCIERR \_ obtener \_ CD                  | No se encontró el archivo o dispositivo MCI solicitado. Intente cambiar los directorios o reiniciar el sistema.                                                         |
| HARDWARE de MCIERR \_                 | El dispositivo especificado exhibe un problema. Compruebe que el dispositivo funciona correctamente o póngase en contacto con el fabricante del dispositivo.                                     |
| MCIERR \_ no válido \_ para la \_ \_ apertura automática | MCI no ejecutará el comando especificado en un dispositivo abierto automáticamente. Espere hasta que se cierre el dispositivo y, a continuación, intente ejecutar el comando.             |
| MCIERR \_ interno                 | Se produjo un problema al inicializar MCI. Intente reiniciar el sistema operativo Windows.                                                                        |
| MCIERR \_ \_ ID. de dispositivo no válido \_      | IDENTIFICADOR de dispositivo no válido. Use el identificador asignado al dispositivo al abrir el dispositivo.                                                                               |
| MCIERR \_ \_ nombre de dispositivo no válido \_    | El dispositivo especificado no está abierto ni reconocido por MCI.                                                                                                     |
| MCIERR \_ archivo no válido \_            | El archivo especificado no se puede reproducir en el dispositivo MCI especificado. Puede que el archivo esté dañado o que use un formato de archivo incorrecto.                               |
| \_falta el \_ parámetro MCIERR       | El comando especificado requiere un parámetro, que debe proporcionar.                                                                                          |
| MCIERR \_ múltiple                 | Se produjeron errores en más de un dispositivo. Especifique cada comando y dispositivo por separado para identificar los dispositivos que provocan los errores.                             |
| MCIERR \_ debe \_ usar \_ Shareable     | El controlador de dispositivo ya está en uso. Debe especificar el parámetro "compartible" con cada comando abierto para compartir el dispositivo.                                  |
| MCIERR \_ no \_ se \_ permite ningún elemento     | El dispositivo especificado no usa un nombre de archivo.                                                                                                               |
| MCIERR \_ ningún \_ entero              | El parámetro de este comando MCI debe ser un valor entero.                                                                                                |
| MCIERR \_ no hay \_ ventana               | No hay ninguna ventana de visualización.                                                                                                                                 |
| MCIERR \_ función no aplicable \_  | La secuencia de comandos MCI especificada no se puede realizar en el orden especificado. Corrija la secuencia de comandos; a continuación, vuelva a intentarlo.                                   |
| MCIERR \_ \_ bloque de parámetros null \_   | Se pasó un bloque de parámetros nulo (estructura) a MCI.                                                                                                       |
| MCIERR \_ \_ de \_ memoria insuficiente          | El sistema no tiene suficiente memoria para esta tarea. Salga de una o más aplicaciones para aumentar la memoria disponible y, a continuación, intente realizar de nuevo la tarea. |
| MCIERR \_ OUTOFRANGE               | El valor del parámetro especificado está fuera del intervalo del comando MCI especificado.                                                                                |
| MCIERR \_ set \_ CD                  | No se puede obtener acceso al archivo o dispositivo MCI especificado porque la aplicación no puede cambiar los directorios.                                                         |
| MCIERR \_ establecer \_ unidad               | No se puede obtener acceso al archivo o dispositivo MCI especificado porque la aplicación no puede cambiar las unidades.                                                              |
| MCIERR \_ recurso sin nombre \_        | No se puede almacenar un archivo sin nombre. Especifique un nombre de archivo.                                                                                                       |
| MCIERR \_ comando no reconocido \_    | El controlador no reconoce el comando especificado.                                                                                                          |
| MCIERR \_ función no admitida \_    | El controlador de dispositivo MCI que usa el sistema no admite el comando especificado.                                                                           |



 

 

 